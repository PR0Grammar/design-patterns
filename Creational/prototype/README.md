# Prototype

## Intent

Specify the kinds of objects to create using a prototypical instance, and create new objects by copying this prototype

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creational/prototype/prototype-struct.png)

## Motivation

Imagine you were designing a software document service. You had two forms of documents: spreadsheet and word document. You want to allow users to seemlessly "copy" their document into another document

The class representing the spreadsheet and word documents might have complex data structures with many private fields, making it hard for clients to easily perform this copy.

Using the Prototype pattern, we can require each document type's class to implement a clone() method that returns a copy of itself (ie. including its state)

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creational/prototype/prototype.png)


