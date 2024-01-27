# Singleton

## Intent

Ensure a class only has one instance nad provide a global point of access to it

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creation/singleton/singleton-struct.png)


## Motivation

Imagine you had a debugger logger for your application that sent out logs across the network. It requires proper order of messages to send and may want to include a batching behavior.

A Singleton can be of use here. We can have a single instance of a LogManager class that can buffer up messages and send them over the wire for logging.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Creation/singleton/singleton.png)
