# Template Method

## Intent

The Template Method pattern allows parent classes to define a 'skeleton' for an algorithm or behavior, but allows the child class to fill in/override specific steps

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Behavioral/template_method/template-method-struct.png)

## Motivation

Imagine you had a encrypted file system service that allowed you to choose your encryption algorithm. Once the content is encrypted, you want to perform some standard operations for compressing and storing the content (ie. stays consistent regardless of encryption algorithm choice). You can use Template Methods to allow for subclasses to provide their own encryption and decryption algorithms.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Behavioral/template_method/template-method.png)

## Applicability

Use Template Methods when:

1. You want clients to only implement certain steps of an algorithm
2. Several classses contain almost identical algorithms with minor differences.
