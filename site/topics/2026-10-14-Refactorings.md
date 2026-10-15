{
"title": "[Internship] Refactorings for live objects",
"layout": "blogpost",
"publishDate": "2026-10-14"
}


## Context

An important activity of software evolution consists in applying refactorings to enhance the quality of the code without changing its behaviour. Having a proper refactoring tool is a must-to in any professional development environment. In addition, live programming allows faster development than the usual edit- compile-debug process. 

During live programming sessions, the developer can directly manipulate instances and modify the state of the running program. However, when a complex refactoring is performed, instances may be corrupted (i.e., their state is lost). For example, when pushing an instance variable to a superclass there is a moment where the superclass does not have yet acquired the new instance variable and the subclass does not have it any more. Itmeans that the value assigned to this instance variable in existing instances
is lost after the refactoring. 

This problem is not anecdotal since 36% of the refactorings described in Fowler’s catalogue corrupt instances when used in a live programming context. There is a need to manually migrate, regenerate or reload instances from persistent sources. This manual fix lowers the usefulness of live programming.

## Objectives

The goal of this project is to revisit the Pharo refactorings and introduce live migration support. 

- Study refactorings that lose instance state
- Extend refactorings with instance migration behavior

## Refs

- B Sarenac, N Anquetil, S Ducasse and P Tesone, A New Architecture Reconciling Refactorings and Transformations, Journal of Computer Languages, 101273, 2024

- P Tesone , G Polito, L Fabresse, N Bouraqadi, S Ducasse, Preserving Instance State during Refactorings in Live Environments, Future Generation Computer Systems, 110, 1-17, Elsevier, 2020 https://rmod-files.lille.inria.fr/Team/Texts/Papers/Teso20a-FutureGeneration-PreservingInstance.pdf


## For the students

Interns should:
- learn fast, for example https://pharo.org
- open minded
- working in an international settings

Student benefits: 
- work on a hot topic
- be immersed in a core language
- learn deep object-oriented design skills 

