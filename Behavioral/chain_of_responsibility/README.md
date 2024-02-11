# Chain of Responsibility

## Intent

Chain of Responisibility (CoR) is a design pattern that lets you forward requests down a chain of handlers. Each handler can determine whether or not to forward the request to the next handler.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Behavioral/chain_of_responsibility/chain-of-responsibility-struct.png)

## Motivation

Imagine you were designing a network routing service that forwards various network requests to a special handler. The last handler will ultimately provide the content for the request, but the request must pass a series of authorization and security tests to valdiate that the request is valid. 

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Behavioral/chain_of_responsibility/chain-of-responsibility.png)

## Applicability

When the CoR pattern when:
1. Your program is expected to process different kind of requests in various ways but the exact type of requests and sequence is not known ahead of time.
2. Service requires executing several methods in order.
3. Set of handlers may need to change at runtime.
