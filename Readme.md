## Day 01 of GO lang learning

### 1. Go Setup and Basics
- [x] Install Go on your machine
    - [x] [Download Go](https://golang.org/dl/)
    - [x] [Install Go](https://golang.org/doc/install)

- [x] Setup Go workspace
    - [x] Create a workspace directory
        ```bash
        mkdir go-workspace
        ```
        to create a workspace directory named `go-workspace` in your home directory. to Practicing Go programs.
    - [x] Set GOPATH environment variable
        ```bash
        export GOPATH=$HOME/go-workspace
        ```
        to set the `GOPATH` environment variable to the workspace directory.

    - [x] Create a `src` directory inside workspace
        ```bash
        mkdir $GOPATH/src
        ```
        to create a `src` directory inside the workspace directory. This is where you will write your Go programs.

    - [x] Create a `hello.go` file inside `src` directory
        ```bash
        touch $GOPATH/src/hello.go
        ```
        to create a `hello.go` file inside the `src` directory. This will be your first Go program.


- [x] Write your first Go program
    ```go
    package main

    import "fmt"

    func main() {
        fmt.Println("Hello, World!")
    }
    ```
    to write a simple Go program that prints `Hello, World!` to the console.
- [x] Understand Go syntax and structure
    - [x] `package main` declares that this file is part of the `main` package.
        `Package main` tells the Go compiler that this program is an executable program rather than a shared library. The `main` package is the entry point of the program.

    - [x] `import "fmt"` imports the `fmt` package, which contains functions for formatting text.
        `import` keyword is used to include packages in your program. The `fmt` package is used to print formatted output to the console.

    - [x] `func main()` is the entry point of the program.
        `func` keyword is used to declare a function. The `main` function is the entry point of the program. When the program is executed, the `main` function is called first.

    - [x] `fmt.Println("Hello, World!")` prints `Hello, World!` to the console.
        `fmt.Println` is a function from the `fmt` package that prints the given text to the console. The text is printed with a newline character at the end.


### 2. Variables, Functions, and Control Structures
- [x] Declare and initialize variables
    - [x] Declare a variable
        ```go
        var name string
        ```
        to declare a variable `name` of type `string`.
    - [x] Initialize a variable
        ```go
        name = "Dhinesh"
        ```
        to initialize the variable `name` with the value `"Dhinesh"`.
    - [x] Declare and initialize a variable
        ```go
        var age int = 25
        ```
        to declare and initialize a variable `age` of type `int` with the value `25`.
    - [x] Declare multiple variables
        ```go
        var (
            city string = "Chennai"
            country string = "India"
        )
        ```
        to declare multiple variables `city` and `country` with their respective values.
    - [x] Short variable declaration
        ```go
        city := "Chennai"
        ```
        to declare and initialize a variable `city` with the value `"Chennai"`. The type of the variable is inferred from the value.
- [x] Define functions
    - [x] Declare a function
        ```go
        func greet(name string) {
            fmt.Println("Hello,", name)
        }
        ```
        to declare a function `greet` that takes a `name` of type `string` as a parameter and prints a greeting message.
    - [x] Call a function
        ```go
        greet("Dhinesh")
        ```
        to call the `greet` function with the argument `"Dhinesh"`.

- [x] Control structures
    - [x] If-else statement
        ```go
        if age >= 18 {
            fmt.Println("You are an adult")
        } else {
            fmt.Println("You are a minor")
        }
        ```
        to check if the `age` is greater than or equal to `18` and print the appropriate message.
    - [x] For loop
        ```go
        for i := 0; i < 5; i++ {
            fmt.Println(i)
        }
        ```
        to print numbers from `0` to `4` using a `for` loop.
    - [x] Switch statement
        ```go
        switch day {
        case "Monday":
            fmt.Println("It's Monday!")
        case "Tuesday":
            fmt.Println("It's Tuesday!")
        default:
            fmt.Println("It's another day!")
        }
        ```
        to check the value of `day` and print a message based on the value.
    - [x] Defer statement
        ```go
        defer fmt.Println("This will be printed at the end")
        ```
        to defer the execution of a function until the surrounding function returns. The deferred function will be executed at the end of the surrounding function.

### 3. Data Structures: Slices, Maps, Arrays

- [x] Arrays
    - [x] Declare an array
        ```go
        var numbers [5]int
        ```
        to declare an array `numbers` of type `int` with a length of `5`.
    - [x] Initialize an array
        ```go
        numbers := [5]int{1, 2, 3, 4, 5}
        ```
        to declare and initialize an array `numbers` with the values `1, 2, 3, 4, 5`.
    - [x] Access elements of an array
        ```go
        fmt.Println(numbers[0]) // prints the first element
        ```
        to access and print the first element of the array `numbers`.
    - [x] Iterate over an array
        ```go
        for i, num := range numbers {
            fmt.Println(i, num)
        }
        ```
        to iterate over the array `numbers` and print the index and value of each element.

- [x] Slices
    - [x] Declare a slice
        ```go
        var names []string
        ```
        to declare a slice `names` of type `string`.
    - [x] Initialize a slice
        ```go
        names := []string{"Alice", "Bob", "Charlie"}
        ```
        to declare and initialize a slice `names` with the values `"Alice", "Bob", "Charlie"`.
    - [x] Append elements to a slice
        ```go
        names = append(names, "David")
        ```
        to append the value `"David"` to the slice `names`.
    - [x] Slice a slice
        ```go
        fmt.Println(names[1:3]) // prints elements at index 1 and 2
        ```
        to slice the slice `names` and print elements at index `1` and `2`.

- [x] Maps
    - [x] Declare a map
        ```go
        var person map[string]int
        ```
        to declare a map `person` with keys of type `string` and values of type `int`.
    - [x] Initialize a map
        ```go
        person := map[string]int{
            "Alice": 25,
            "Bob": 30,
            "Charlie": 35,
        }
        ```
        to declare and initialize a map `person` with key-value pairs.
    - [x] Access elements of a map
        ```go
        fmt.Println(person["Alice"]) // prints the value for key "Alice"
        ```
        to access and print the value for the key `"Alice"` in the map `person`.
    - [x] Iterate over a map
        ```go
        for name, age := range person {
            fmt.Println(name, age)
        }
        ```
        to iterate over the map `person` and print the key-value pairs.

### 4. Error Handling

- [x] Error interface
    - [x] Declare an error
        ```go
        var err error
        ```
        to declare an error variable `err` of type `error`.
    - [x] Create a custom error
        ```go
        err = errors.New("Something went wrong")
        ```
        to create a custom error message `"Something went wrong"` and assign it to the error variable `err`.
    - [x] Check for an error
        ```go
        if err != nil {
            fmt.Println(err)
        }
        ```
        to check if the error variable `err` is not `nil` and print the error message.

- [x] Error handling
    - [x] Function with error return
        ```go
        func divide(a, b float64) (float64, error) {
            if b == 0 {
                return 0, errors.New("Division by zero")
            }
            return a / b, nil
        }
        ```
        to define a function `divide` that takes two `float64` arguments and returns the result of division and an error if the divisor is zero.
    - [x] Handle error in caller
        ```go
        result, err := divide(10, 0)
        if err != nil {
            fmt.Println("Error:", err)
        } else {
            fmt.Println("Result:", result)
        }
        ```
        to call the `divide` function and handle the error returned by the function.

### Resources
- [Go Official Documentation](https://golang.org/doc/)
- [Learn Go with Tutorials](https://golangbot.com/)
