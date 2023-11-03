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
