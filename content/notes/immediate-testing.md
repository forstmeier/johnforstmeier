---
title: "Immediate Testing"
date: 2020-12-22T10:45:00-05:00
draft: false
tags: [
	"software",
]
---
Continuously testing entire code repositories increases the ability to introduce rapid changes. Being able to do this in early stages, such as the MVP, is highly valuable.

Simple approaches, like adding a `unit_tests` script to the repo containing just a `go test ./... -coverage` command [[1](https://golang.org/pkg/cmd/go/internal/test/)][[2](https://blog.golang.org/cover)] achieve this. Even though it would initially be triggered manually, doing so would provide value to the developer even before a complete CI/CD pipeline could be established.