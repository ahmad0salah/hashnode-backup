## Treating Primitive Obsession with Value Objects

## Primitive Obsession

Primitives are friendly familiar faces, they are the default tyes we reach for whenever we are writing code and for a good reason. They are convenient and we are very familiar with them.

But this overusing the primitive types and the tendency to use them to represent almost everything. Especially when representing seemingly simple abstractions like a measuring unit, postal code, or an email field.

What is wrong with that you might ask?

There are few issues with making primitives represent domain objects.

## Breaking encapsulation

When you use primitive values, you will break encapsulation. How many times will you need to verify or transform a type in your application?
Thinking about temperature, we might add a validation upon storing the value and again when updating it.

Now, think about all the places where you will need to display temperature. You will duplicate this code!

## Value Objects to the rescue 

Value objects are just classes but with a couple of important features.

### 1. Value Object can answer equality check

If we wanted to represent a currency as a <amount, currency> and later wanted to check if two points are equal. unless you are careful with your code you may get the wrong answer.
Therefore, value objects must implement a correct equality check method.

### 2. Value Object should be immutable
What we gain from delegating the equality check to the object. can lead to  [aliasing bugs](https://martinfowler.com/bliki/AliasingBug.html) 

Aliasing as defined by Martin Fowler is "Aliasing occurs when the same memory location is accessed through more than one reference. Often this is a good thing, but frequently it occurs in an unexpected way, which leads to confusing bugs."

This can happen when dealing with value objects as we blur the lines between values and reference.

As we have seen implementing value objects requires some extra work to make your development faster you may consider using a library that helps you with that. If you are using C# I would recommend  [ValueOf](https://github.com/mcintyre321/ValueOf)  & for Java people, you can use the  [@Value](https://projectlombok.org/features/Value)  annotation from Lombok

Further reading on  [implementing Value Objects](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/implement-value-objects) 

