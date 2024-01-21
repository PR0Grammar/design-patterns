# Builder

## Intent

Separate the construction of a complex object step by step

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creational/builder/builder-struct.png)

## Motivation

Imagine you wanted to construct a Pizza class that let's you change different properties before throwing it in the oven and letting it cook.

Imagine the Pizza has the following properties that you can set:
- Toppings
- Size
- Hand-toss/Pan
- Sauces
- Cheese

You could in theory have a very large constructor that takes in the properties you want to make a Pizza instance. Alternatively, you can use the **Builder** pattern to help construct the object step by step and only perform steps that are necessary (for example, toppings are optional)

If we take this further, suppose we have a set of products that we sell for an Order. We can optionally have a **Director** that builds the individual products of the Order for fufilment. For example, we might also sell Cake and Chicken Wings, which will have their own Builder classes. Once the items are built out, the Director can fulfil the order.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creational/builder/builder.png)

## Applicability

Use the Builder pattern when:
- The algorithm to create a complex object should be independent of the parts that make up the object
- The construction process must allow different representations for the object that's constructued


## Benefits/Consequences

1. Allows varying of a product's internal representation
	- The interface for a builder hides the representation and internal structure of the product. It also hides how it gets assembled. (eg. How are toppings stored? What happens if you remove a topping?).

2. Isolates code from construction and representation
	- Improves modularity by encapsulating the way a complex object is constructed and represented

3. Gives finer control over the construction process.
	- Unlike creational patterns that make a product in one shot (eg. Factory methods), the Builder is step by step. Only once the product is complete do we retrieve the final form. 


## Techniques

1. Assembly and construction interface
	- Using a Builder interface for many products, you want the methods to be generalized enough to handle all concrete builder usecases.
	- Sometimes builders simply just "append" parts as its being constructued, but sometimes (like in the topping for Pizza), we would need to acccess the parts of the product added before. Appropriate data structures for the parts should be considered

2. Why no abstract class for products?
	- In the common scenario, the products produced by the concrete builders differ so greatly in their representation that there is little to gain from giving different products a common parent class. Although in the Order example above, the differnt products share the eat() method, there likely isn't many commonalities between the products. Therefore a shared interface isn't really required.

