---
layout: post
title:  "Agile Software Design - Summary"
date:   2018-12-01 20:24:00 -0300
categories: [software, desing]
---


I'm a big fan of the book *Agile Software Development, Principles, Patterns and Practices*, I consider it is the bible about Software Development. One the main subjects
explained is **Agile Design**. In follow I describe the principal concepts involved.

## What Is Agile Design?

The desing of software projetc is an abstract concept. It has to do with
the overall shape and structure of the program as well as the detailed shape and sctructure of each module, class, and method. It can be 
represented by many different media, but its final embodiment is source 
code. In the end, the source code is the desing.

The book describes the five principles to guide the software design, when all principles are applied, is possible to minimize the odors on the source code and improve more quality for the software.

## Desing Smell - The Odors of Rotting Software

1. Rigidity - The System is hard to change because every change forces many other changes to other parts  of the system.
2. Fragility - Changes cause the system to break in places that have no conceptual relationship to the part that was changed.
3. Immobility - It is hard to disentangle the system into components that can be reused in other systems.
4. Viscosity - Doing things rigth is harder than doing things wrong.
5. Needless Complexty - The desing contains infrastructure that adds no direct benefit.
6. Needless Repetition - The desing contains repeting structures that could be unified under a single abstraction.
7. Opacity - It is hard tp read and understand. It does not express its intent well.

## The Principles

1. SRP - The Single Responsability Principle
2. OCP - The Open-Closed Principle
3. LSP - The Liskov Substituion Principle
4. DIP - The Dependency Inversion Principle
5. ISP - The Interface Segregation Principle


### SRP - The Single Responsability Principle

> *A class should have only one reason to change.*

### OCP - The Open-Closed Principle

> *Software entities (classes, modules, functions, etc.) should be open 
> for extension, but closed for modification.*

### LSP - The Liskov Substituion Principle

The LSP can be paraphrased as follows:

> *SUBTYPES MUST BE SUBSTITUTABLE FOR THEIR BASE TYPES.*

Barbara Liskvo fist wrote this principle in 1988. She said:

> *What is wanted here is something like the follwing substitution
> property: If for each object `o1` of type `S` there is an object `o2`
> of type `T` such that for all programs `P` defined in terms of `T`,
> the behavior of `P` is unchanged when `o1` is substituted for `o2` 
> then `S` is a subtype of `T`.*


### DIP - The Dependency Inversion Principle

> a. *High-level modules should not depend on low-level modules.
> Both  should depend on abstractions*
> b. *Abstractions should not depend on details. Details should 
> depend on abstractions*


### ISP - The Interface Segregation Principle

> *Clients should not be forced to depend on methods that they do not use.*

This principle deals  with the disadvantages of "fat" interfaces.
Classes that have "fat" interfaces are classes whose interfaces
are not cohesive. In other words, the interfaces of the class can be 
broken up into groups of methods. Each group serves a different set of 
clients. Thus, some clients use one group  of memmber functions, 
and other clients use the other groups.

The ISP ackoenledges that there are objects tha require noncohesive interfaces; however, it suggest that clients should no know about them 
as a single classs. Instead, clients should know about abstract base 
classes  that have cohesive interfaces.
