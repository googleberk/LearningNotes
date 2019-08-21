# notes1

1. write-ahead logging: The changes are first recorded in the log, which must be written to stable storage, before the changes are written to the database; all modifications are written to a log before they are applied.


    The purpose of this can be illustrated by an example. Imagine a program that is in the middle of performing some operation when the machine it is running on loses power. Upon restart, that program might need to know whether the operation it was performing succeeded, succeeded partially, or failed.
    
    (1). succeeded: the program wants to write data ```hello```, if it successfully writes ```hello``` to a buffer(still in the middle of perfoming this operation) before the power goes off, then when it resumes, it will compare to what was in the log, writing ```hello```, which means it will do nothing, since it already write ```hello```(keep things as they are).
    
    (2). succeeded partially: before the power goes off, the program only write ```hell```(no ```o``` at the end), then when it resumes, it will compare the log, and complete what it had started.
    
    (3). failed: before the power goes off, the program write ```dog``` which is wrong, then when the program restarts, it will compare the log, and found out that it was supposed to write ```hello```, but it wrote ```dog```,(which is wrong), therefore, it needs to undo what it had started(already written ```dog```), and start writing the correct ```hello``` from the begining. 
    
    If a write-ahead log is used, the program can check this log and compare what it was supposed to be doing when it unexpectedly lost power to what was actually done. On the basis of this comparison, the program could decide to undo what it had started, complete what it had started, or keep things as they are.
    
2. ???(answer: see 4.3 below) ```type Buffers```: link here: https://golang.org/pkg/net/#Buffers.Read. I am not quite sure about the meaning/usage of ```func (v *Buffers)``` here in ```func (v *Buffers) Read(p []byte) (n int, err error)```. It seems like Buffers is a ```type Buffers [][]byte```, 

3. some notes on this link:https://syslog.ravelin.com/byte-vs-string-in-go-d645b67ca7ff

    ```[]byte``` is something like this:
    
    ```c
        type slice struct {
           data uintptr
           len int
           cap int
        }
    ```
    ```string``` is something like this:
    ```c
        type string struct {
            data uintptr
            len int
        }
    ```



4. link here: http://www.golangbootcamp.com/book/methods.

    4.1: the difference between ```method``` and ```function```
    Note: A frequently asked question is “what is the difference between a function and a method”. A method is a function that has a defined receiver, in OOP terms, a method is a function on an instance of an object.
    
    4.2: So far we’ve seen ```Printf```, which prints the formatted string to os.Stdout. ```Sprintf``` formats and returns a string without printing it anywhere. Example:
link: https://gobyexample.com/string-formatting
    ```c
        s := fmt.Sprintf("a %s", "string")
        fmt.Println(s)
    ```
    4.3: Go does not have classes. However, you can define methods on struct types. ```Greeting()``` is a method that defined on struct ```User```. See the following code:
    ```c
    type User struct {
	    FirstName, LastName string
    }

    func (u User) Greeting() string {
	    return fmt.Sprintf("Dear %s %s", u.FirstName, u.LastName)
    }
    ```
    The method receiver appears in its own argument list between the func keyword and the method name. so it is clear that the method receiver in this case is ```(u User)```, and that means, a ```User struct``` instance have a method ```Greeting()```. we can do ```u.Greeting()``` in our code. 
    
    Note how methods are defined outside of the struct, if you have been writing Object Oriented code for a while, you might find that a bit odd at first. The method on the User type could be defined anywhere in the package. In the above code, it means that method ```Greeting()```need not be in ```User struct```, we can simply def a connect a function ```Greeting()``` in this case to the ```User struct``` by putting ```(u User)``` after the keyword ```func```.
    
    4.4: link here: https://www.golangprograms.com/example-arrays-of-arrays-arrays-of-slices-slices-of-arrays-and-slices-of-slices.html
    
    
    4.5: the second answer in this Stack Overflow page is good: https://stackoverflow.com/questions/7703251/slice-of-slices-types. 
    
    Also notice the usage of ```range``` in the demo code:
    ```c
    func main() {
        ss := make([][]uint8, 2) // ss is []([]uint8)
        fmt.Printf("ss:    %T %v %d\n", ss, ss, len(ss))
        for i, s := range ss { // s is []uint8
            fmt.Printf("ss[%d]: %T %v %d\n", i, s, s, len(s))
        }
    }
    ```
    
    At first, I don't know why ```s``` would be **Type** ```[]uint8``` in ```for i, s := range ss```, later I find a useful link: https://gobyexample.com/range, and the code and notes below makes me understand this:
    ```c
    for i, c := range "go" {
        fmt.Println(i, c)
    }
    ```
    
     >range on strings iterates over Unicode code points.
     >The first value is the starting byte index of the 
     >rune and the second the rune itself.
    
    
    By the way, the way ```range``` is used in Go is very interesting. I think under different data structures, range is used differently.
    
     >range iterates over elements in a variety of data
      >structures. Let’s see how to use range with some
      >of the data structures we’ve already learned.

    Also, one important thing to notice is that: **Multi-dimensional slices are jagged and are analogous to multi-dimensional jagged arrays.** ```slices``` in Go is jagged. See the meaning of [jagged array](https://en.wikipedia.org/wiki/Jagged_array). Arrays of arrays are implemented as [lliffe vectors](https://en.wikipedia.org/wiki/Iliffe_vector).
    
    


    