# Abstract Factory

## Intent

Provide an interface for creating families of related or dependent objects without specifying their concrete classes

AKA: **KIT**

# Motivation/Problem

Imagine a beverage producer that makes three products: `Coffee`, `Soda`, `Tea`

Each of beverages has two variations: `Sweetened` and `Non-Sweetend`

We need a way to create each type of bevergae object.


The solution here is to create an abstract BevergaeFactory class that declares an interface for creating each type of beverage.
