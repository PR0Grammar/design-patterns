# Decorator

## Intent
Attach additional responsibilities to an object dynamically. Decorators provide a flexible alternative to subclassing for extending functionality.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/decorator/decorator-struct.png)


## Motivation

Imagine you owned a service that booked flights. After some time, you wanted to offer additional things that people can add-on to their flights (lodging, car rentals). The initial design of your application was designed solely around flights, with a reserve() method that reserved the flight.

Offering the different mix-and-match options (eg. flight+lodge, flight+car, flight+car+lodge) can be done through concrete classes for each permutation, but this can grow very fast. Instead, you can utilize a Decorator to "wrap" each option for a reservation/booking. 


![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/decorator/decorator.png)

## Applicability

Use Decorator when:
- You need to be able to assign extra behaviors to objects at **runtime** without breaking the code that uses these objects
	- In this above example, we "wrap" the initial booking with additional options at runtime, depending on the user's wants. However, the flight booking logic still remains in-tact regardless of these additional options.
- When it's awkward/not possible to extend an object's behavior using inheritance
- You want to allow for the ability for responsibilites to be withdrawn
	- We may remove the option for hotel booking later. We can simply just remove the Decorator and its usage instead of refactoring Booking.

