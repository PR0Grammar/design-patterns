# Abstract Factory

## Intent

Provide an interface for creating families of related or dependent objects without specifying their concrete classes

AKA: **KIT**

# Motivation/Problem

Imagine a bottler that bottles different beverages for differnt brands

Brands: Coke, Pepsi, DrPep 
Each of these brands has sells their own type of beverge: Coffee, Tea, Soda, Water


We need a way to create each type of bevergae for the different brands.

The Solution: Create interfaces and classes for each beverage type and introduce a BeverageBrandFactory. 


The BeverageBrandFactory is an **Abstract Factory** - an interface for the factories to create the different products. In our case, we want each concrete factory to produce coffee, tea, soda and water. We will have a concrete factory for each brand.
