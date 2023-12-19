
# Go Basic Fundamentals: Hello, world.  

Questions to answer:  
* How do we run the code in our project? 
* What does `package main` mean?  
* What does `import "fmt"` mean?  
* What's that `func` thing?  
* How is the `main.go` file organized?  


## Running Go Code with CLI Commands  
The answer to the question:  
* How do we run the code in our project? 
```bash  
go run main.go  
```

### CLI Commands Available with Go  
```bash  
go build  
go run  
go fmt  
go install  
go get  
go test  
```

| Command   | Result 
|-----------|--------  
| `build`   | Compiles a bunch of Go source code files.  
| `run`     | Compiles and executes one or more files.  
| `fmt`     | Formats all the code in each file in the current directory.  
| `install` | Compiles and "installs" a package.  
| `get`     | Downloads the raw source code of someone else's package.  
| `test`    | Run any tests associated with the current project.  
`get` and `install` are for handling dependencies.  

### `go run` vs `go build`
`go run` compiles and executes a program. It does not leave behind a binary.  
`go build` is used to only compile a program, and does not execute it.  

## Packages & `package main`
A Package is a project or workspace. It's a collection of common source code files.  

Any file with `package main` at the top will belong to the same package, and therefore  
 the same workspace.  

### Types of Packages  
In Go, there are two different types of packages. 
1. Executable: Generates a file that we can run.  
    * Spits out an executable when compiled.  
2. Reusable: Code used as "helpers". Good place to put reusable logic.  
    * Code dependencies or libraries.  
    * The sort of code that can be used across multiple projects (such as classes in other  
      languages).  

How do you know what type of package you're making?  
You know you're making an executable type package when it is named `main`.  
Specifically the word `main` is for compiling executables.  
* Note: Somewhere in `package main`, you *must* have a `func main()`.  

If the package name is not `main`, it will not produce an executable.  
Any other package name than `main` (i.e., `package calculator`) means that you're  
writing a "reusable" or "dependency" type package.  
* Note: If you have a `func main()` inside a package that is not `package main`, you  
  can still run `go build` on it, but it will not produce an executable.  


## Import Statements  

Import statements should import packages with double quotes.  
It's used to give our package access to code that's inside of another package.  
The `fmt` package is part of the Go Standard Library.  

We're not limited to packages in the Go stdlib.  
We can use `import` to import reusable packages authored by other engineers.  

### Packages in the Go Standard Library  
[See all packages in the Go Standard Library](https://golang.org/pkg).  
Below is a list of *some* of the packages that Go offers in its stdlib.  
* `fmt`
* `io`
* `math`
* `debug`
* `encoding`
* `crypto`



## Functions in Go  
```go  
func main () {
    // function body  
}
```
Broken down:  
* `func`: Tells Go we're about to declare a function.  
* `main`: Sets the name of the function.  
* `()`: List of arguments to pass to the function.  
* `// function body`: A comment in the function body. Calling the function runs this code.  


## How Go files are organized  
1. Package declaration.  
2. Import other packages that you need.  
3. Declare functions and tell Go to do things.  

All Go files follow this simple structure.  



