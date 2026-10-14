{
"title": "[Internship] Fast Typechecks for Pharo",
"layout": "blogpost",
"publishDate": "2026-10-14"
}


## Context

Typechecks are frequent in object-oriented programming, even if good design tends to avoid them. 
In Pharo several reflective parts of the system are using them. For example, the announcements are heavily relying on them.

````
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

## Displays at work

A solution is to cache some information about the superclass chain inside the class itself. 

Imagine the following hierarchy

```
A 
	B 
	C
D
	E
```
Each class gets a “display” that represents it superclass chain.

```
A 	A
B	A B
C 	A C
D 	D
E	D E 
```

The following expresses how using such display we can know if a class is a subtype of another one

```
	B isKindOf: A
	<=>    
	( B display at: A depth ) = A
```

Since the display can be of limited size we could check if 
A depth > display size and in such case do the slow lookup.


## Objectives

The intern will:

- Study metaclass implementation
- Implement such mechanism
- Measure the improvement
- Measure the memory cost of a display and find a good compromise (auto tuning of it).  

## Refs

- Rohan Padhye and Koushik Sen, Efficient Fail-Fast Dynamic Subtype Checking, VMIL 2019, https://rohan.padhye.org/files/failfast-vmil19.pdf

- Cliff Click and John Rose, Fast subtype checking in the hotspot JVM article, JGI 2002

