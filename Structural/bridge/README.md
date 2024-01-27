# Bridge

## Intent

Decouple an abstraction from its implementation so that the two can vary independently

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/bridge/bridge-struct.png)

## Motivation

Imagine you had a bottling factory for different bevergas: Soda, Coffee. You had two brands you bottle for: Coke and Pepsi.

You want to compose the two things (brand and beverage type) to be able to bottle bevergaes for each brand. You could have each brand have a subclass for each beverage type which we can then use to bottle the beverage (eg. CokeSodaBottler, PepsiSodaBottler). However this becomes complex as as grow the number of brands and number of beverages types (for an additional brand in the current state, we'd introduce two new subclasses, for example). 

Instead we can use the Bridge pattern to have allow for the two concepts to vary independently. We can have the brand classes _contain_ the beverage type class.For any bottling operations, each brand class can simply delegate to the beverage class it has.


![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/bridge/bridge.png)

## Applicability

Use the Bridge pattern when

- You want to avoid permanent binding between abstraction and its implementation (eg. creating subclasses for each beverage-brand pair is much harder to reverse). 
- Both the abstractions and their implementations should be extensible by subclassing _and_ you want to avoid the growing complexity in the number of subclasses as implementations increase. (eg. more bevergae types doesn't introduce N subclasses for each brand)

