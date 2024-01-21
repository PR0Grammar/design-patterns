# Abstract Factory

## Intent

Provide an interface for creating families of related or dependent objects without specifying their concrete classes

AKA: Kit

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creational/abstract_factory/abstact-factory-struct.png)

## Motivation/Problem

Imagine a bottler that bottles different beverages for differnt brands

Brands: Coke, Pepsi, DrPep 
Each of these brands has sells their own type of beverge: Coffee, Tea, Soda, Water


We need a way to create each type of bevergae for the different brands.

The Solution: Create interfaces and classes for each beverage type and introduce a BeverageBrandFactory. 


The BeverageBrandFactory is an **Abstract Factory** - an interface for the factories to create the different products. In our case, we want each concrete factory to produce coffee, tea, soda and water. We will have a concrete factory for each brand.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creational/abstract_factory/abstract-factory.png)


## Applicability

Best used under the following conditions: 
- A system should be independent of how its products are created, composed, and represented
- A system should be configured with one of many families of products
- A family of related product objects is designed to used together and you can enforce this (via the interfaces)
- You want to provide a class library of products and just want to expose the interface, not implementation.
	- eg. PepsiFactory.createWater() vs new PepsiWater()

## Benefits and Consequences 

1. Isolation of concrete classes
	- The client gets isolated from the implementation classes since the factories are responsible for the object creatin. Clients manipulate the instances thorugh their abstract interfaces. Product classes (eg. PepsiWater) are isolated in the implementation fo the concrete factory - they do not appear in client code

2. Makes exchanging product families easy
	- If a usecase for the client simply switches the concrete factory of one family to another (eg. Pepsi to Coke), it changes all the underlying products at once.

3. Promotes consistency among products
	- When product objects (eg. Water, Tea) are designed to work together, it's important that the usecase only uses one family (eg. Coke) at a time. The AbstractFactory pattern makes this easy to enforce.


## Techniques

1. Factories as singletons
	- Usually you only need one instance of the factory per product family, so it's best to implement them as singletons

2. Prototypes for many families
	- If there are many product families, a concrete factory can be implemented using the Prototype pattern. The concrete factory is initialized with a prototypical instance of each product in the family (eg. Water, Tea) and it creates a new product by cloning its prototype. The Prototype approach eliminates the need to make a concrete class for each new family

3. Defining extenisble factories
	- As noted, adding a new product requires updating the AbstractFactory interface and all the concrete factory classes. A more flexible, but less "safe" way to do this is assign an idenitifer to each product (a integer, enum.. whatever) and have a single make() method for the factories that takes in that idenitifer.



