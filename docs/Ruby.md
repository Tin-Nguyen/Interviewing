1. Is the line of code below valid Ruby code? If so, what does it do? Explain your answer.
```
-> (a) {p a}["Hello world"]```

Answer:
Yes, it’s valid. Here’s how to understand what it does:

The -> operator creates a new Proc, which is one of Ruby’s function types. (The -> is often called the “stabby proc”. It’s also called the “stabby lambda”, as it creates a new Proc instance that is a lambda. All lambdas are Procs, but not all Procs are lambdas. There are some slight differences between the two.)

This particular Proc takes one parameter (namely, a). When the Proc is called, Ruby executes the block p a, which is the equivalent of puts(a.inspect) (a subtle, but useful, difference which is why p is sometimes better than puts for debugging). So this Proc simply prints out the string that is passed to it.

You can call a Proc by using either the call method on Proc, or by using the square bracket syntax, so this line of code also invokes the Proc and passes it the string “Hello World”.

So putting that all together, this line of code (a) creates a Proc that takes a single parameter a which it prints out and (b) invokes that Proc and passes it the string “Hello world”. So, in short, this line of code prints “Hello World”.

2. What is the difference between calling super and calling super()?
Answer:
A call to super invokes the parent method with the same arguments that were passed to the child method. An error will therefore occur if the arguments passed to the child method don’t match what the parent is expecting.

A call to super() invokes the parent method without any arguments, as presumably expected. As always, being explicit in your code is a good thing.

3. What differencies between the codes below:
```
x = hello
x += " world"
```
and 
```
x = hello
x.concat " world"
```
Answer:
```
foo = "foo"
foo2 = foo
foo.concat "bar"

puts foo
=> "foobar"
puts foo2
=> "foobar"

foo += "baz"
puts foo
=> "foobarbaz"
puts foo2
=> "foobar"```

4. Can you call a private method outside a Ruby class using its object?
Yes, with the help of the `send` method.

Given the class Test:
```
class Test
   private
       def method
         p "I am a private method"
      end
end
```
We can execute the private method using send:
```
>> Test.new.send(:method)
"I am a private method"
```

5. Given this input:
```
x = [{"a" => 10},{"b" => 20},{"c" => 30}]
```
How can you obtain the following?
- one array containing all keys
- another containing all values
- the sum of all the values
Answer:
```
This works:
```
y = x[0].merge(x[1]).merge(x[2])

y.keys                   # will return all keys
y.values                 # will return all values
y.values.inject(:+)      # will return the sum of all values
```
But a better first line would be this:
```
y = x.reduce(:merge)
```
…because it would work on an array of any size, not just the exact input given.```