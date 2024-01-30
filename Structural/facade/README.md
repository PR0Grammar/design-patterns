# Facade

## Intent

A structural design pattern that provides a simplified interface to a library or framework

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/facade/facade-struct.png)

## Motivation

Imagine you had a food delivery system. The parts of the system include a Driver, the Food, and the Payment.

When making an order, it can get complex having all these operations be performed directly on the client. Instead, we can make a simple Facade to handle finding a Driver, charging the card on file for the Payment, and getting the Food order request to the restaurant.


![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/facade/facade.png)

## Applicability

Use the Facade pattern when:

- You have a limited and straightforward interface to a set of complex systems
  - It works as a great "fast" solution to meet client requirements when dealing with many complex systems

- When you want to structure a system into layers
  - Defines an entryponint into each logical "grouping" that makes sense. Communication to the underlying systems happen through the Facade.
