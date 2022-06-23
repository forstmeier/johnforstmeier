---
title: "Software Method Design"
date: 2022-06-20T10:18:06-04:00
draft: false
---
This is a high-level outline of my current approach to method design in software. It's not groundbreaking - it's more just my working mental model.

Methods are split into two types:

1. Manipulators
2. Managers

**Manipulators** are responsible for in-memory actions like creating or updating resources - for example `struct` types representing domain objects. **Managers** do the storing and fetching of those `struct` types to and from the persistence layer.

By keeping these two method types _very_ separate, code is easily decoupled. Definining them in their own `interface` types, implementing them in their own package, and then exporting them to their callsite makes for a highly mentally comprehensible and easily tested codebase.
