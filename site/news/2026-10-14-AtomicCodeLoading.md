{
"title": "[Internship] Atomic code loading in a dynamic life programming environment
",
"layout": "blogpost",
"publishDate": "2026-10-14"
}


Potential location:  Lille, France

Team: EVREF INRIA LILLE

Supervisor: Stéphane Ducasse stephane.ducasse@inria.fr (https://Ducasse.github.io)


### Presentation

Updating applications during their execution is used both in production to minimize application downtime and in integrated development environments to provide live programming support. Nevertheless, these two scenarios present different challenges making Dynamic Software Update (DSU) solutions to be specifically designed for only one of these use cases.

We want to revisit gDSU the solution proposed by Dr. P. Tesone in his PhD. 

The entry point of the gDSU engine is a patch. A patch is a collection of changes that describe the update to perform. It includes the changes to apply in the code, such as method and class modifications, and the corresponding
state migration logic. gDSU generates this patch semi-automatically by applying a version control system (VCS) version diﬀ or/and by recording code changes made in the IDE during a development session. 

### Objectives

The objectives are part of a larger project that is how to update the code update. We focus here on the first part: how to update the running software in an atomic manner. 

The first part of the solution proposed by Tesone is a smart partial copy of the system to be updated, an update of this partial copy with modifications (additions, removals) and a bulk pointer swapping that literally swaps old classes/methods/instances with updated ones. Then he proposed a quiessence model where all the threads can be stopped and even programs on the execution stack can be updated.

The goal of the topic is to revisit such an approach in modern Pharo (https://www.pharo.org) versions.  

- Design and perform a partial copy of the program to be updated based on the actual changes to be performed. 
- Use bulk pointer swapping to update the program.
- Iterate to be able to update core libraries.

###  Refs: 

- Tesone Pablo, Mise à jour Dynamique pour Environnemts de Production et Programmation Interactive
https://theses.fr/2018MTLD0012
- Chapter two of the PhD presents a state of the art of existing approaches

### Quality of the students

- learn fast, for example https://pharo.org
- open to alternative ways of looking at computation (swapping pointers under the feet of a program is a disruptive by efficient way but it requires thinking :).