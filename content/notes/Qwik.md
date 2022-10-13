---
title: "Qwik"
alias: []
---
*A no hydration instant on personnalized web app with thymeleaf.*

The startup time of you application si key to make users stay and come back to the site.

**Javacript** is mostly the issue when it comes to performance.

Even in the top 50 websites, js is still really slowing things down.

## How to fix Javascript ?

With Qwik, the complexity of hte application doesn't impact the startup time.

In the past :
- php
- ruby on rails
- jquery
=> was  performent, but the dev was slow

Now:
- angular
- view
- react
- ...
=> fast dev, scales, unified model but super slow

future:
- Google wiz
- Qwick
- Marko v6

=> easy to build AND fast 

## Advantages of Qwick
Focuses on **startup time**

### Resumable
The app can skip the javascript bootup process (hydration). The state of the app is serialized and sent as html to the browser without any startup time.

The app can start just like a VM that has been paused and resumed.

With resumable frameworks, few JS is downloaded, it's loaded when the user interracts with the page.

### Demo
When you click on a button, the JS specific to that button is DL, not even the framework gets downloaded.

Everything gets serialized, even functions.

Quick looks quite like react when developping.

***$*** : marks lazy loading points

**The javascript can also be delayed until the user scrolls and the component gets visible !**
(default behaviour)

> [!INFO] 
>Only the complexity of a specific operation will impact the performance of that operation. It doesn't impact the rest of the app or the startup time.

There is a service worker anticipating what the user could do and downloads the JS on a separate thread in the meantime (still only linked to what's visible).

### Personnalization


