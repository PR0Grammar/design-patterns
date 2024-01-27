# Adapter

## Intent
Convert the interface of a class into another interface clients expect. Adapters let classes work together that couldn't otherwise because of incompatible interfaces.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/adapter/adapter-struct.png)

## Motivation

Imagine you had a calendar service that had time represented in strings with their TimeZone. You want to integrate with a third-party service that deals with time with the UNIX epoch (number). You want to delegate some of the operations you are doing now to the third party, but don't want to change your existing data format.

You can use an Adapter to handle this. The Adapter will implement the interface for the client, but format and delegate the operation to the third party service

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/adapter/adapter.png)

## Applicability

- You want to use an existing class and its interface does not match the one you need
- You want to create a reusable class that cooperates with unrelated or unforeseen classes (classes that don't conform to the interface)



