# C++ Basics

---
## 1. Comments

```c++
/* C-Style Comments must be enclosed like this and can span
an arbitrary number of lines. And can also end
in the middle of one */ std::cout << "Hello World!";
```

Comments are completely ignored by the compiler
- because the Preprocessor has already removed them
- C-Style comments cannot be nested!

```c++
/* nested C-Style Comments /* are bound */
 to produce nasty effects */
```

```c++
// C++-Style comments look like this...
// ... and span the remainder of the line
```

```c++
// C++-Style comments will disable /* C-Style Comments:
std::cout << "Hello World!";
```

```c++
/* C-Style comments will also disable 
// C++-Style Comments: */ std:: cout << Hello World!";
```

```c++
// But you cannot end one with the other */ (this is still a comment)
```

---

## 2. Output with cout
```c++
cout << "Hello World" << endl;
int i = 10;
cout << "i is" << i << endl;
```

- `cout` writes text to the `standard output` (normally: text console)
- `<<` is called the `stream operator`
- `endl` is a special value and represents
  - a line break
  - and a signal to `flush` the `output buffer`
- output is `buffered`
  - it is not written immediately
  - but collected for some time
  - and then written in one go
  - for performance reasons
