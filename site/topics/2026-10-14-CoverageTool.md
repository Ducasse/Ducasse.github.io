{
"title": "[Internship] Branch Coverage Tool",
"layout": "blogpost",
"publishDate": "2026-10-15"
}


## Context

Pharo has a coverage tool defined in the package Coverage. However, it is not really robust. 
The objective of this internship to address this problem.

Here is an example of Coverage collection. 

```
| collector coverage |
collector := CoverageCollector new. "Instantiate"
collector methods: Point methods, Rectangle methods.  "Configure with the methods to watch."
coverage := collector runOn: [ (1@1 corner: 2@2) center ].  "Setup, execute and teardown."
(coverage methods includes: Point>>#x) >>> true.  "Inspect the results"
(coverage nodes size > 10) >>> true. "Covered paths are also available"`
````

## Objectives

Using MethodProxies defines a coverage tool that reports the number of executions of messages in a method. Using such an information and some static analysis, devise a branch coverage tool.


## Tasks 

The intern will:

- Study method proxies.
-  Using a visitor (check the chapters 1 and 2 of [https://github.com/SquareBracketAssociates/Booklet-FunWithInterpreters/releases/download/latest/index.pdf](https://github.com/SquareBracketAssociates/Booklet-FunWithInterpreters/releases/download/latest/index.pdf) or the API of OCProgramNode get the list of all the message send in a method.
- Study the current implementation of coverage as available in the package Coverage and Coverage-Tests. One objective is to develop the same behavior but without the use of reflectivity.
- Create a separate package where you duplicate the Coverage classes. 
- Apply the coverage on some test suite. 
- Study Mutalk https://github.com/avl-univ-lille/testing/blob/2024/practice/1-mutation.md
- Use Mutalk the mutation testing framework of Pharo to guide you on how to improve the coverage of some tests.


## Refs

- First chapter of https://github.com/SquareBracketAssociates/Booklet-FunWithInterpreters
- MethodProxies is a library that can annotate any messages send in Pharo (except optimized messages that are not message sent such as ifTrue:ifFalse:). https://github.com/pharo-contributions/MethodProxies
- https://github.com/avl-univ-lille/testing/blob/2024/practice/1-mutation.md
## For the students

Interns should:
- learn fast, for example https://pharo.org
- open minded
- working in an international settings

Student benefits: 
- work on a hot topic
- be immersed in a core language
- learn deep object-oriented design skills 

