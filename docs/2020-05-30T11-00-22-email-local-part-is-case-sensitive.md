---
date: 2020-05-30T11:00:22-07:00
title: Email Local Part Is Case Sensitive
tags: 
---

# Email Local Part Is Case Sensitive

RFC 2821, 2.4: "The local-part of a mailbox MUST BE treated as case sensitive."

In other words, "example@test.com" and "Example@test.com" are different email addresses, however "example@test.com" and "example@Test.com" are not.

That's pants-on-head stupid.