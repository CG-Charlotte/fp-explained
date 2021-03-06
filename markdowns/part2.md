# Higher Order Function

In functional programming, a function is defined as a "first order citizen". 
This means it includes all the properties generally available to any other element, such as the possibility of being affected to a name, returned as a result or passed as a parameter.

A higher-order function is a function that accepts other functions as parameters and/or use a function as the return value.  
Let's try it out!
Implement the greeting function to return "Hello, [name]" if the name is defined. Otherwise, return "who are you?".

## More detailed informations
[Check the scaladoc!] (http://docs.scala-lang.org/tutorials/tour/higher-order-functions.html)

## How to pass a function as a parameter?
```scala
def apply(f: Int => String, v: Int) = f(v)
```


@[Greetings]({"stubs":["/src/main/scala/example/Hof.scala"], "command":"example.TestHof"})

What make high order functions awesome is this ability to pass a function in parameter. 

Let's try to implement the following example: we want to use different sorts. Let's try to use the already-implemented sort function to define the other ones.

_ Language tips _
For this example you can use the wildcard character _ which can match any parameter. It's useful to compare elements to each other.

@[Implement the differents sort]({"stubs":["/src/main/scala/example/HofSort.scala"], "command":"example.TestHofSort"})

You can use functions of the collection API the same way you use map and reduce.
