## Useful features from c++ 11

To build with C++ 11 use the following: 
`g++ -std=c++11 *.cpp`

### auto 
In c++ 11, auto can be used for variable initialization and function-> return type. The compiler determines and the type and replaces the auto keywork with the type. e.g. const auto& i = expr, the type of i is exactly the type of the argument u in an imaginary template template<class U> void f(const U& u) if the function call f(expr) was compiled. Therefore, auto&& may be deduced either as an lvalue or rvalue reference according to the initialized, which is used in range-based for loop. 


### Lambda function
In C++11, a lambda expression—often called a lambda—is a convenient way of defining an anonymous function object right at the location where it is invoked or passed as an argument to a function. Typically lambdas are used to encapsulate a few lines of code that are passed to algorithms or asynchronous methods.

E.g. see emplace_back example


### emplace_back for vector

E.g. Threads cannot be copied and only have move symantics. In older c++ we would have to resize the stack and move the thread. In the new c++ you can pass the constructor arguments to emplace_back and that should be able to create an object directly in the vector's memory instead of requiring construction and then move. 

The constructor argument to a thread is just a callable function so we can write the following : 

```
std::vector<std::thread> threads;

threads.emplace_back([i]
      {
         std::cout << " Hello world: " << i <<  std::endl;
      })
```

### Range based loop 
Executes a for loop over a range.
Used as a more readable equivalent to the traditional for loop operating over a range of values, such as all elements in a container.

e.g. 

```
for (auto& [first,second] : mymap) {
   // use first and second

}
```


### Auto pointer 


### thread_sleep



