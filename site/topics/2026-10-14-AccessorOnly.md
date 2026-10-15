{
"title": "[Internship] Accessors all the way down",
"layout": "blogpost",
"publishDate": "2026-10-14"
}


## Context

By default pharo supports direct field accesses. 
Some languages like Self did the inverse: any direct accesses 
were in fact accessors. 

## Measuring the impact of converting all direct accesses into accessors



Now since developers may have define accessors for their own classes, we cannot just generate accessors and replace direct accesses to them using a simple refactoring.

The goal of this topic is to 
- generate hidden accessors
- change the compiler to use such hidden accessors
- we could avoid to have double accessors calls when subclasses do not specialise existing ones.



## Objectives

The intern will:

- Study metaclass implementation
- Implement such mechanism
- Measure the improvement
- Measure the memory cost of a display and find a good compromise (auto tuning of it).  

## Refs

- Rohan Padhye and Koushik Sen, Efficient Fail-Fast Dynamic Subtype Checking, VMIL 2019, https://rohan.padhye.org/files/failfast-vmil19.pdf

- Cliff Click and John Rose, Fast subtype checking in the hotspot JVM article, JGI 2002

## Quality of the students

Intern should:
- learn fast, for example https://pharo.org
- open minded
- working in an international settings

Student benefits: 
- work on a hot topic
- be immersed in a core language
- learn deep object-oriented design skills 

