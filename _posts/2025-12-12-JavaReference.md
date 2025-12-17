---
layout: post
title: Java Pass by Reference vs Pass by Vlaue
date: 2025-12-12 14:24:00
description: Coming soon
tags: formatting charts
categories: sample-posts
chart:
  plotly: true
---

# Java Pass by Refernce or Pass by Value

I'm going over C++ as a refresh to prepare for my upcoming semester taking an offical course on **Computer Architecture & Assembly Lang**, Even though it's goint to be just a touch of C and probably no C++. Non the less, its's something that i think every Software Engineer and Student of Computer Science should get very comfortable with.

C/C++ are, in my opinion, the corner stone of modern software engineering programming languages. Take a look at `Go`, trying to compete by having `goroutines` and being a **compiled** language. Or `Rust`, the *Memory* safe and *Concurrency* secure language of choice. But at the end, companies from Jane Street, Citdent to Boring Company, and Google are looking for competent C/C++ developers. In part, learning C++ will help with understanding why its so fun to use something like `python`


> "If I have seen further, it is by standing on the shoulders of giants"
> - Sir Isaac Newton in a 1675 letter, meaning his scientific breakthroughs

So a great question i ask during interviews and when i join lunch with my team is, "Is Java Pass by Reference or Pass by Value?". The younger Junior devs are the ones im intrested in learning from to keep up with the times in what they are intrested in. Talk to an old head who had to use `COBOL` and thats when the discussion gets spicy with side tracked topics of different compilers, paragims, etc..



### Pass by Reference

So, what is pass by reference?

Lets use C++. We can have pointers to a variable

```C++
int x = 4; // create an int (4 bytes) and assign it to the value 4
int *xP = &x; // create a pointer of type int (4 bytes) and assign it to reference, x
```

Doing a `std::cout << xP << endl;` would yeild me somethign like `0x7fffdc4b0a2c`, which is a address in the stack.
If i `dereference` the pointer by `*xP`, then i can get the assigned value of `4`;


Ok, its a bit much if we are looking at this for the first time. Lets digest this diagram before continuing.

```
+-------------------------------+       +-------------------------------+
|             Stack             |       |             Heap              |
| (grows downward)              |       | (grows upward)                |
+-------------------------------+       +-------------------------------+
| int a = 10;     | address: 0x1000 |    
| int b = 20;     | address: 0x1004 |    
| int c = 30;     | address: 0x1008 |    
|                               |       |                               |
| int* ptr;       | address: 0x1010 |       +-------------------------------+
| ptr → 0x2000 ---------------------------> | int thisNum = 100; | addr: 0x2000 |
|                               |       |                               |
+-------------------------------+       +-------------------------------+

Later: ptr = new int(100);  // allocation on heap
*ptr == 100                 // dereferencing gives the Value
```

we can see that `*ptr` is initialized at address `0x1010` then later its assigned the same address as `int thisNum` at address `0x2000`
We have `ptr` and `thisNum` both pointing to the same address in memory.


lets take this example for C++ passing by reference.

```C++
void incrementByReference(int& x) // Note the & indicates that this is a reference/pointer to memory address
{
    x++;                    
}

int main()
{
    int a = 10;
    
    incrementByReference(a); // --> this will change the value to 11
    std::cout << "After passing by Reference :: " << a << endl;

    return 0;
}
```

So, we can see that we manipulated the value of `a` and changed it in another method. `&x` means that its pointing to the same address as `a`. This will go to that address, and increment its value by 1.


Lets look at passing by value now

```C++
void incrementByValue(int x) // Creates a local copy
{
    x++;
}

int main() 
{
    int y = 200;

    incrementByValue(y); // value y, in the main() scope remains 200.
    
    std::cout << "After passing by Value :: " << y << endl;

    return 0;
}
```

In this example, we take the `y` and pass it in the method `incrementByValue` which then makes a local variable for its own function scope to use. After this scope is returned we loose reference to that copy by auto garbage collection much like `Java`.




