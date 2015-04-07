---
layout: post
title: 'Ken Scambler: Run free with the monads: Free Monads for fun and profit'
comments: true
share: true
categories:
- scala
tags:
- scala
- scalaz
- free monad
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

<p><iframe width="560" height="315" src="https://www.youtube.com/embed/fU8eKoakd6o" frameborder="0" allowfullscreen></iframe></p>

Ken Scambler ([@KenScambler](http://twitter.com/kenscambler)) in this talk deftly takes us through how we can _effectively_ separate concerns within our software.  This is an essential feature of being able to write code that can be reasoned about locally, and hence easier to maintain.

The technique is to use `Free` monads.

Free monads allow you to separate the definition of your programme from the running of it.  In this talk Ken demonstrates a tank game that has a defined script but different AIs that can be applied later through the use of _swappable_ interpreters.

The key to the free monad is to have a side-effect Free "Fantasy" DSL that describes your concerns and an Interpreter which executes the effects.  The Free monad lifts your DSL (which is a functor) into monad.

Ken is also available for Weddings and Children's parties.

You can find the talk [on YouTube](https://youtu.be/fU8eKoakd6o).