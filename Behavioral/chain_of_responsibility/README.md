# Chain of Responsibility

## Intent

Chain of Responisibility (CoR) is a design pattern that lets you forward requests down a chain of handlers. Each handler can determine whether or not to forward the request to the next handler.

## Motivation

Imagine you were designing a network routing service that forwards various network requests to a special handler. The last handler will ultimately provide the content for the request, but the request must pass a series of authorization and security tests to valdiate that the request is valid. 


## Applicability

When the CoR pattern when:
1. Your program is expected to process different kind of requests in various ways but the exact type of requests and sequence is not known ahead of time.
2. Service requires executing several methods in order.
3. Set of handlers may need to change at runtime.
