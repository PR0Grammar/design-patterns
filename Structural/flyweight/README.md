# Flyweight

## Intent
Allows for reusability of common state between objects to reduce memory usage

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/flyweight/flyweight-struct.png)

## Motivation

Imagine you had a Messaging service that had many unique users. The Messaging service can use metadata about a person (eg. profile picture, phone number/email, etc) to display to the user. The individuals a person talks to can appear in more than one thread (eg. 1-1 threads, group threads). You could repeat this metadata for each individual in each messaging thread, but that can quickly add up as the number of messaging threads increase.

Instead you can use a Flyweight to cache this metadata for each individual, then perform operations needed for each messaging thread with this state.


![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/flyweight/flyweight.png)


## Applicability

Use a Flyweight when:
- You need to support a large number of objects and need to be diligent with memory usage
    - Not much to add... pretty straightforward.
