# Introduction

## The big ball of mud

"It takes clear direction and persistent energy to stop Software solutions from
devolving into a *big ball of mud*(chaos).

## Abstraction and encapsulation

These are *OOP* concepts designed to hide low level implementations--state behaviour
and data--behind high level *classes* and or *functions*.

## Layering

This is another high level concept to combat the slow degradation of Software solutions into chaos.
Primarily, this concept requires a software to have three different layers:

1. Presentation layer (front-end)
2. Business logic
3. Database layer

There are well defined rules to follow on how the layers should interact;
and what code implementation should go where.

## The Dependency Inversion Principle

This concept is still quite fuzzy to me at the moment.
But here is my current understanding.

### *High-level* implementation must not depend on *low-level* implementation, both must depend on **Abstraction**

Basically, the business does not care how the *low-level* modules work, as 
long as they work. The *high-level* modules are what matter and should
never be strongly coupled with *low-level* ones. For example, If changed
the implementation of a formula that I wrote in *numpy* it should not kill the application. There should be another layer of *Abstraction* between the
modules that call the low-level modules at least to reasonably handle
the errors when they exist.


### **Abstraction** should not depend on *details*, instead *details* should depend on **Abstraction**