## [Protocol and Value Oriented Programming in UIKit Apps](https://developer.apple.com/videos/play/wwdc2016/419/)

Protocol and Value Oriented Programming is a way to make _local
reasoning_ possible.

Using classes, which are copied by reference, might hurt local
reasoning, as someone external entity can change the class that
we are using simply because it has a reference to it.

Using value types we guarantee that no code can change our
values from underneath us.

**Retroactive Modelling**:

```swift
protocol MyProtocol {
  // ...
}

// MyClass already has the properties and methods that MyProtocol defines, so
// we can retroactively make MyClass conform to MyProtocol
extension MyClass: MyProtocol { }
```

Using generics allows the compiler to make optimizations, since
they give it more information about the types involved in the
code.

You can do nifty things with protocols and generics, like:

```swift
protocol FooProtocol {
  associatedtype Bar
}

struct Foo<T: FooProtocol>: FooProtocol {
  // Define the actual type of the associated type Bar from the protocol as
  // whatever the type of the give T.Bar is.
  //
  // Note that the fact that T and Foo both conform to FooProtocol is simply
  // to stay in line with the example in the session.
  typealias Bar = T.Bar
}
```

- Local reasoning with value types
- Generic types for fast, safe polymorphism
- Composition of values

Having a *single code path* and *order independence* helps a lot with local reasoning.

Enums are perfect to map mutually exclusive values.

You can use enums to map the view state. You gain:

- mutually exclusive states
- state changes all at once

_Yes! That's what I've been trying to do for a while now ^^_.

Takeaways:

- Customization through composition
- Protocols for generic, reusable code
- _Taking advantage of value semantic_
- _Local reasoning_
