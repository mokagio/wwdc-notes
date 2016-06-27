## [Protocol and Value Oriented Programming in UIKit Apps
](https://developer.apple.com/videos/play/wwdc2016/419/)

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

_Left at 20:00_
