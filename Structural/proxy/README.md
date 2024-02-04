# Proxy

## Intent

The Proxy pattern provides a substitute or placeholder for another object. It controls access to the original object and can perform things before and/or after sending the request to the original object

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/proxy/proxy-struct.png)

## Motivation

Imagine you had a database for your service that performs the usual CRUD operations on a set of entities for your business. The API used to access the database operations is simplisitc - it'll just execute the given query by the clients. However, this leads to vulnerabilities if there is a malacious client that's looking to run a dangerous query (eg. maybe delete user accounts without permission). Moreso, there might be business logic we need to run prior to ensure only authorized clients are accessing the database.

This is where a Proxy can come in. A Proxy can expose the underlying database API, but prior to running the actual operations for the database, can perform sanitzation of queries and client authorizations.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Structural/proxy/proxy.png)

## Applicability

Use the Proxy pattern when:

- You want to have lazy initialization (virtual proxy)
  - Some objects can be heavyweight for an application and may not even be utilized. We can delay the creation until actually required (eg. a marketplace where the user can buy items from many sellers. The order is only finalized when the user charges their card for the items, so no need to perform any changes to the sellers' items/inventory _until_ the order is complete)
 
- Access control (protection proxy)
  - As highlighted in the "Motivation" section, limits who gets to use a service
 
- Local execution of a remote service (remote proxy)
  - Proxy passes request over the network, but appears to be "local"
 
- Logging requests (logging proxy)
  - Useful if we want to log some/all requests made to a service before actually handling the request 
