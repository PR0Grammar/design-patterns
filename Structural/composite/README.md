# Composite

## Intent
Compose objects into tree structures to represent part-whole hierarchies. Composite lets clients treat individual objects and compositions ob objects uniformly

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/composite/composite-struct.png)


## Motivation
Imagine you had a freight ship that carried containers. These containers can carry loads of items, including other containers. You want to be able to derive properties from the whole of the containers (eg. tonnage).

You could calculate the individual parts of the cargo (eg. the container weights AND the items they carry) and aggregate them up. But the Composite pattern here would help derive these properties in a simpler manner. A ShipContainer can contain other ShipContainer.


![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/composite/composite.png)

## Applicability

Use the Composite pattern when:

- You want to represent part-whole hierachies of objects
	- In other words, you want to implement a tree-like **object** structure. Simple idea: leave items + complex containers (that contain other containers or leaves).
- You want clients to be able to ignore the difference between compositions of objects and individual objects (eg. The individual cargo items vs the containers for the ship). Clients will treat all objects in the composite structure uniformly
	- All elements in the Composite pattern share a common interface. The client doesn't have to worry which its dealing with.




