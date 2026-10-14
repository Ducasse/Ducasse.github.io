{
"title": "[Internship] Fast Announcements",
"layout": "blogpost",
"publishDate": "2026-10-14"
}


## Fast Announcements

Keywords: Lookup, Benchmarks

### Context
Announcements are often used to decouple parts of a subsystem. A part will notify other parts that registered interest. In Pharo, they are heavily used for system updates and UI events in forthcoming modern UI frameworks (Bloc and Toplo).

```
	anAnnouncer when: MouseOver do: aBlock
```

However, announcements are often structured in terms of hierarchies; this implies a lookup to so that a registered action for a parent class actually works for the subclasses. 

The following methods are the heart of the checks:

```
SubscriptionRegistry>>handleSubscriberClass: eventClass
	"Return true if the receiver has a callback subscribed for the event class"
	^ subscriptions anySatisfy: [ :sub |
			(sub subscriber class == eventClass) or:
			[ sub subscriber class includesBehavior: eventClass ] ]

Behavior >> includesBehavior: aClass

	self isTrait ifTrue: [ ^false ].
	^self == aClass or:[self inheritsFrom: aClass]

Behavior >> isKindOf: aClass
	"Answer whether the class, aClass, is a superclass or class of the receiver.
	The current implementation allows for a Trait to be used as argument"

	^ self class == aClass or: [ self class inheritsFrom: aClass ]

Behavior >> inheritsFrom: aClass
	"Answer whether the argument, aClass, is on the receiver's superclass
	chain."
	
	| aSuperclass |
	aSuperclass := self superclass.
	[aSuperclass == nil]
		whileFalse:
			[aSuperclass == aClass ifTrue: [^true].
			aSuperclass := aSuperclass superclass].
	^false
```

We see that announcements are doing systematic class lookup. This lookup is costly.

### Objectives

This raises the question of avoiding the cost of such lookup.

The intern will: 

- Study subclasses of `Announcement` as well as the implementation.
- Benchmark: we should analyse the cost of having hierarchies when dispatching announcements. 
- Two paths are possible: a kind of compilation process that would flatten such (often narrow) hierarchies into a flat structure or optimize the isKindOf: logic 
- Implement an efficient isKindOf: mechanism using 'displays'

### Refs

- Rohan Padhye and Koushik Sen, Efficient Fail-Fast Dynamic Subtype Checking, VMIL 2019, https://rohan.padhye.org/files/failfast-vmil19.pdf

- Cliff Click and John Rose, Fast subtype checking in the hotspot JVM article, JGI 2002

