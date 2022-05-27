---
title: "Code Ignorance Obfuscation"
date: 2022-05-27T09:18:16-04:00
draft: false
---
Following test-driven development [[1](https://en.wikipedia.org/wiki/Test-driven_development "Test-driven development - Wikipedia")] can compensate for broad gaps in knowledge of the language being used.

For example, situations where _values_ are passed instead of _pointers_ or some tricky `break` statement can all be accounted for in the test suite. If the code is modular enough and the tests are fairly exhaustive, the actual implementation doesn't really matter - as long as the **contract between the method and the tests is respected, you don't need to know how it makes anything happen**.

One caveat is lower-level optimizations; those will still require a deeper understanding of the language in question in order to implement them correctly.
