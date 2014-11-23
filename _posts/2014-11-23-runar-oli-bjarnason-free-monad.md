---
layout: post
title: 'Rúnar Bjarnason: CompositionalApplication Architecture With Reasonably Priced Monads'
comments: true
share: true
categories:
- scala
tags:
- scala
- scalaz
- free monad
- coproduct
- monad
- functor
- ADT
status: publish
type: post
published: true
author:
  login: chris@chrisandjo.com
  email: chris@chrisandjo.com
  display_name: Chris
  first_name: ''
  last_name: ''
---

This talk is not embeddable but you can find it [here](https://parleys.com/play/53a7d2c3e4b0543940d9e538/).

Runar ([@runarorama](http://twitter.com/runarorama)) takes us through an experimental approach of separating the intent of an application from its effects, thus making it massively extensible.  In this talk he steers away from using monad transformers and large monad stacks, which can be some what awkward in Scala.  Instead, he opts for a "flat" script in a `for-comprehension` which describes your programme in a referentially transparent way.

He proposes using Algerbraic Data Types to describe the interactions in your system such as logging, authentication, database and user input and then lifting them into the `Free` monad.  Then through the use of monad Co-products the effects chain can be flattened into a very nice API.

The advantage of using the free monad is that the interpretation of the effects are done separately from the pure logic.  This makes testing applications very simple as "test" interpreters can be written and injected into the system.  Moreover, changing between different implementations are very easy as it _only_ involves writting a new interpreter, for instance, switching from a relational database to a document store.

You can find the talk [here on Parleys](https://parleys.com/play/53a7d2c3e4b0543940d9e538/) and [the slides here](https://dl.dropboxusercontent.com/u/4588997/ReasonablyPriced.pdf).