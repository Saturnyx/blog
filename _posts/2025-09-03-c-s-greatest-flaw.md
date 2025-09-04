---
layout: post
title: C++'s Greatest Flaw
description: "C++ is a great language, but it has its downsides."
date: 2025-09-03 21:55 +0800
categories: programming
---

_I was busy coding a library for my Vex V5 Robot when I stumbled upon an error_
_It wasn't just any ordinary error, it was an error occurring after compilation_
_- a runtime error. "Uggh! This is gonna be so difficult to fix" I think to_
_myself._

---

## What is C++?

C++ is a high-level, general-purpose programming language created by Danish
computer scientist Bjarne Stroustrup in 1985. It was written as an extension of
the C-language and is known for its performance, efficiency, and flexibility of
use. C++ is widely used in today's world with approximately 70–90% of commercial
games (especially AAA titles) and 20-40% of desktop apps written in C++.

## The big problem with C++

> "C makes it easy to shoot yourself in the foot; C++ makes it harder, but when
> you do it blows your whole leg off"
>
> ~ Bjarne Stroustrup

Every language has its weakness, regardless of how powerful it is. C++ came with
great speed and performance, but it had one problem: C++ ain't secure.

### Memory Issues

C++'s lack of support for garbage collection means that C++ requires manual
memory management. Developers must explicitly allocate and deallocate memory,
which can lead to memory leaks, dangling pointers, and other memory-related
errors if not handled carefully. C++ offers low-level memory access through
pointers, which, while powerful, can introduce vulnerabilities like buffer
overflows and other security issues if not managed correctly.

### C++ isn't easy

C++ syntax is notorious for being hard to learn even for experienced coders. It
has many features and paradigms. The syntax is more complex and less-intuitive
as compared to other languages. Testing and Debugging are also difficult due to
more complex error messages and crashes. Again, the lack of automatic memory
management makes coders have to manually manage memory as described above.
While C++ has great community support and a vast number of libraries, the
ecosystem is fragmented compared to other languages. Moreover, dependency
management is not as straightforward and more difficult to use. Build systems
such as [CMake](https://cmake.org/) and [Make](https://www.gnu.org/software/make
/) are rather complex and hard to use, especially for beginners.

### Portability Issues

Remember how I started by telling you that C++ is a high-level language? That
isn't exactly true... C++, while being written like a high-level language, is
capable of accessing many low-level systems such as memory and hardware. This
also poses an issue where a C++ program in one system might not work on another
system due to reliance on platform-specific features. This can lead to
compatibility issues and increased development effort when targeting multiple
platforms.

## What can we do?

### Safer Memory Management

To counter C++'s memory vulnerabilities, you can use more memory safe languages
such as [Rust](https://www.rust-lang.org/). If you would like to learn about the
differences between C++ and Rust, you can check out
[this blog]({% post_url 2025-08-17-c-or-rust-differences-explained %}). It is
also recommended that you thoroughly learn how to manage memory in C++ before
you start coding.

### Start with easier languages

In this world, there are so many languages besides C++. For beginners, I
recommend languages like [Python](https://www.python.org/) and [Go](https://go.d
ev/). Both of these languages are based on simplicity while still being used
widely. If you are up for it, you can try [Java](https://www.java.com/en/), its
syntax is similar to C++'s. These languages have easier to use dependency
managers and build systems which will seem easier to use for beginners. You have
two options - Either take more time and dedication to climb the steep learning
curve or pick a simpler language to act as a stepping stone. At the end of the
day, it is your choice on which path you'll choose.

## Conclusion

C++ is a great language, but it also has its own downsides. This doesn't mean
that you have to quit C++ entirely, maybe you can choose another solution or
even create one - there are many ways to tackle the problem of C++.

---

_I refer to the C++ documentation about treading. Hmm... Perhaps it was time I_
_looked into relearning C++, with the time and effort this time._
