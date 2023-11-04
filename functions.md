## FUNCTIONS

### A function to create the math times table;

```swift

func printTimesTable(number: Int) {
    for i in 1...12 {
        print("\(number) * \(i) is \(number * i) ")
    }
}
printTimesTable(number: 10)

```

```swift
func printTimesTable(number: Int, end: Int) {
    for i in 1...end {
        print("\(number) * \(i) is \(number * i) ")
    }
}
printTimesTable(number: 20, end: 40)
```

### function to check if a string contains the same letters, regardless of their order.

```SWIFT
// function to check if a string contains the same letters, regardless of their order.
func checkString(name1: String, name2: String) -> Bool {
    if name1.sorted() == name2.sorted() {
        return true
    }
    return false
}

let result = checkString(name1: "lEo", name2: "olE")
print(result)
```

```SWIFT
// Another example.
func areLettersIdentical(string1: String, string2: String) -> Bool {
    return string1.sorted() == string2.sorted()
}
```

### Function for pythagoras theorem

```swift
func findPythagoras(a: Double, b: Double) -> Double{
    sqrt(a * a + b * b)
}

print(findPythagoras(a: 3, b: 4))
```
