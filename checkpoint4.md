### Please attempt to solve it on your own first before looking at the solution.

Checkpoint 4 of the Hacking With Swift #100daysofSwiftUI

Write a function that accepts an integer from 1 through 10,000, and returns the integer square root of that number.

You can’t use Swift’s built-in sqrt() function or similar – you need to find the square root yourself.

If the number is less than 1 or greater than 10,000 you should throw an “out of bounds” error.

You should only consider integer square roots – don’t worry about the square root of 3 being 1.732, for example.

If you can’t find the square root, throw a “no root” error.

```swift

enum RootError: Error {
    case noRoot, outOfBounds
}

func findIntSquareRoot(_ number: Int) throws -> Int {
    if number < 1 || number > 10_000 {
        throw RootError.outOfBounds
    }
    for i in 1...100 {
        if number == i*i {
            return i
        }
    }
    throw RootError.noRoot
}
let input = 100
do {
    let result = try findIntSquareRoot(input)
    print("Square root of \(input) is \(result).")
} catch RootError.outOfBounds {
    print("\(input) is out of bounds")
} catch RootError.noRoot {
    print("\(input) is not a perfect square root.")
} catch {
    print("Error.")
}

print(findIntSquareRoot(81))

```
