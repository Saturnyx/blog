---
layout: post
title: What is Mojo?
description: "The next new Python? How do I use it?"
date: 2025-08-22 09:37 +0800
categories: programming-news
---

_"What are the best Python implementations?", I type into Google. I was_
_searching for a Python implementation that can cross-compile my programs to_
_binaries. That was when I came across an implementation I have never came_
_across - Mojo. I started researching on this new language..._

---

## What is Mojo?

> "Mojo unifies high-level AI development with low-level systems programming.
> Write once, deploy everywhere - from CPUs to GPUs - without vendor lock-in."
>
> ~ [Modular.com](https://www.modular.com/mojo)

[Mojo](https://www.modular.com/mojo) is a language developed by [Modular](https:
//www.modular.com) that combines benefits of multiple languages such as:

- Python
- C++
- Rust
- Zig

It claims to provide bare-metal performance comparable to that of C++ while
holding the flexibility and readability of Python, allowing for faster
prototyping and development. Mojo also has native support for NVIDIA and AMD
GPUs (Graphical Processing Units).

## Applications

Mojo can be used in many places, but primarily is used in developing LLMs (Large
Language Models) and other AI models. Its support for GPUs makes it highly
suitable replacement for Python in AI training. Mojo also supports existing
Python libraries such as [Pytorch](https://pytorch.org/) and [Tensorflow](https:
//www.tensorflow.org/). It's bare-metal performance also gives it an edge over
Python. However, Python is not likely to get fully replaced by Mojo. Rather,
both Mojo and Python will be used together, just like how C++ and Python are
currently used together.

## Getting Mojo

Mojo currently only supports MacOS, Linux and WSL (Window Subsystem for Linux)
platforms. You can refer to [this page](https://docs.modular.com/mojo/manual/get
-started/) in their docs to download and install Mojo. Also, if you are a
Windows user like me, you probably have to use WSL or some other virtualization
platform. [This guide](https://learn.microsoft.com/en-us/windows/wsl/install)
will help you install WSL on your system. From then on, you can continue with
the standard installation on bash.

---

_I finally setup my Hyper-V Virtual Machine (Hyper-V is a platform similar to_
_WSL). I run the installation command. "Installation failed. error: ..." it_
_returns. AARGH!!! Seems like the installation is not as easy as it seems..._
