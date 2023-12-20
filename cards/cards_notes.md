
# Cards - A Package that Simulates Playing Cards  

A module that will simulate different actions using playing cards.  

## Functions  
This package will have the following functions:  
| Function Name     | What it Should Do 
|-------------------|-------------------  
| `newDeck`         | Creates a list of playing cards. Essentially an array of strings.  
| `print`           | Log out all the contents of a deck of cards.  
| `shuffle`         | Shuffles all the cards in a deck.  
| `deal`            | Create a `hand` of cards.  
| `saveToFile`      | Save a list of cards to a file on the local machine.  
| `newDeckFromFile` | Load a list of cards from the local machine.  


## Variables  
Create and assign a variable:  
```go  
var card string = "Ace of Spades"  
```
Broken down:  
* `var`: Tell Go we're about to create a new variable.  
* `card`: The name of the variable will be "card".  
* `string`: Only a string will *ever* be assigned to this variable.  
* `"Ace of Spades"`: Assign the value "Ace of Spades" to this variable. 

Go is a **Statically Typed Language**, like C, C++, or Java. 
* This means that it has **static types**.  
    * After a variable is declared, it can *only* contain the type that it was given.  

As opposed to **Dynamically Typed Languages**, like JS, Ruby, or Python.  
* Essentially means that we do not care what values we assign to any given variable.  
    * e.g., in Python we can do `number = 1`, and then `number = "One"`.  
    * So the variable `number` can change types just by redefining it.  

### Other Ways of Assigning a Variable  
In Go, you can use the *walrus operator* (`:=`) to assign a variable without  
specifying a type.  
The Go compiler will automatically infer, and assign the correct type based on the RHS.  
* Note: The syntax `:=` is *only* used when **defining a new variable**.  
    * Assigning an existing variable a new value, only use the assignment (`=`) operator.  
```go  
card := "Ace of Spades"  
card = "Five of Diamonds"  
```
You can also declare your variable, and then assign it a value separately:  
```go  
var card string  
card = "Ace of Spades"  
```

---  

You can declare variables outside of the function:  
```go  
var card string  
func main() {
    card = "Ace of Spades"  
    fmt.Println(card)  
}
// Ace of Spades  
```
This is valid.  
However, if you try to assign the variable outside the function, you'll get a compiler error:  
```go  
var card string = "Ace of Spades"  
func main() {
    fmt.Println(card)  
}
// ERROR  
```

## Basic Go Types  

A **NON-EXHAUSTIVE** list of some **basic** types:  
| Type      | Example  
|-----------|--------  
| `bool`    |  `true`/`false` 
| `int`     |  `0`, `-1000`, `9999`
| `string`  |  `"Sup!"`, `"How YOU doin?"`
| `float64` |  `10.000001`, `0.00009`, `-100.003`

These are the ones you'll probably be using the most often.  



