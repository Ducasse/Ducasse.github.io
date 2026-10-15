{
"title": "[Internship] Branch Coverage Tool",
"layout": "blogpost",
"publishDate": "2026-10-15"
}


## Context

Pharo used to have a coverage tool. However it was not really robust. 
The objective of this internship to address this problem.

Using MethodProxies defines a coverage tool that reports the number of executions of messages in a method. 
Using such information and some static analysis (visitor), devise a branch coverage tool.




## Tasks 

The intern will:

- Study method proxies
- Study the current implementation of coverage as available in the package Coverage and Coverage-Tests

```
| collector coverage |
collector := CoverageCollector new. "Instantiate"
collector methods: Point methods, Rectangle methods.  "Configure with the methods to watch."
coverage := collector runOn: [ (1@1 corner: 2@2) center ].  "Setup, execute and teardown."
(coverage methods includes: Point>>#x) >>> true.  "Inspect the results"
(coverage nodes size > 10) >>> true. "Covered paths are also available"`
````

## Refs

Ref: 
MethodProxies is a library that can annotate any messages send in Pharo (except optimized messages that are not message sent such as ifTrue:ifFalse:). https://github.com/pharo-contributions/MethodProxies
- https://github.com/pharo-contributions/MethodProxies

## For the students

Interns should:
- learn fast, for example https://pharo.org
- open minded
- working in an international settings

Student benefits: 
- work on a hot topic
- be immersed in a core language
- learn deep object-oriented design skills 

