# Factory Method

## Intent

Define an interface for creating an object, but let subclasses decide which class to instantiate.

Also known as: Virtual Constructor

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creational/factory_method/factory-method-struct.png)

## Motivation/Example

Imagine you had to design a system that introduced a handy-man for the various businesses you support. The handy-man would have specific skills to service the business they are trained in helping. 

Let's say you help the following businesses: Restaurant, Movies, and DryCleaner

You can create an interface that allows you to create a handy-man object for each business.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creational/factory_method/factory-method.png)


## Applicability

Use the Factory Pattern when:
- A class cannot anticipate the class of objects it must create (eg. which type of handy-man do I create?)
- A class wants its subclasses to specify the object it creates
- classes delegate responsibility to one of several helper subclasses and you want to localize the knowledge of which helper subclass is the delegate


## Benefits/Consequences

1. Avoid the need to bind application-specific classes into you code (eg. We don't care about the underlying handy-man's skillset, just that they are a handy-man)

2. If the client has to subclass the Creator (eg. BusinessThatNeedsHandyman) just to use create a concrete object (eg. RestauarantHandyMan), then it becomes another vector of growth for the class.

3. Provides hooks for subclasses
- Factory Methods provide subclasses with hooks for providing extended version of an object. If say the Movies wants to supply different type of handy-man, it can do so as long as the object that is returned is a HandyMan

4. Connects parallel class hierachies
- In the above example, the client is aware of the HandyMan and is aware of the BusinessThatNeedsHandyMan. The subclasses themselves create concrete objects of their specific type (eg. Movies->MoviesHandyMan).


## Techniques

1. Parameterize factory method

A variation of the pattern is to let a factory method create multiple kinds of a product via a parameter (eg. enum, int). 

