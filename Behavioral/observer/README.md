#Observer

## Intent

Observer is a behavioral design pattern that enables a subscription mechanism for objects that care about specific events.

![alt text](https://github.com/PR0Grammar/design-patterns/blob/main/Behavioral/observer/obsever-struct.png)

## Applicability

Use the Observer pattern when:

- Canges to state require updating other objects where the other objects may not be known ahead of time
  - Events generally are omitted without a care about the receiver(s). The receiever(s) can handle the event as they'd like.
 
- Objects in your app need to observe others, but only for limited time or specific cases.
