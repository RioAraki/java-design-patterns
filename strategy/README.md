---
layout: pattern
title: Strategy
folder: strategy
permalink: /patterns/strategy/
categories: Behavioral
tags:
 - Gang of Four
---

## My overview
Strategy pattern 光看这个代码的例子可能并不那么容易理解背后的motivation，这个 [youtube 视频](https://www.youtube.com/watch?v=v9ejT8FO-7I)
可能对为什么需要 strategy pattern有所帮助。以这个例子来说，如果例子本身更复杂，比如屠龙勇士有多种不同的职业，并且每个职业有攻击方式、外观、技能等多个methods，
那本能的我们可能会用oop的思路，把屠龙勇者作为一个 abstract class，里面有攻击方式，外观，技能三个 methods。但这种设计有个问题，即
不同职业的部分methods相同，比如战士职业和刺客职业的攻击方式是一样的（都是近战），圣骑士和牧师职业的技能是一样的（都是会血），这种不同methods之间的重复组合会
导致很多重复的代码，那用 strategy pattern可以把所有 method 设计成接口，在对每个接口的不同methods做具体实现。这样最终设计职业时只要调用每个接口下需要的methods就行了。
## Also known as
Policy

## Intent
Define a family of algorithms, encapsulate each one, and make them
interchangeable. Strategy lets the algorithm vary independently from clients
that use it.

## Class diagram
![alt text](./etc/strategy_1.png "Strategy")

## Applicability
Use the Strategy pattern when

* Many related classes differ only in their behavior. Strategies provide a way to configure a class either one of many behaviors
* You need different variants of an algorithm. for example, you might define algorithms reflecting different space/time trade-offs. Strategies can be used when these variants are implemented as a class hierarchy of algorithms
* An algorithm uses data that clients shouldn't know about. Use the Strategy pattern to avoid exposing complex, algorithm-specific data structures
* A class defines many behaviors, and these appear as multiple conditional statements in its operations. Instead of many conditionals, move related conditional branches into their own Strategy class

## Tutorial 

* [Strategy Pattern Tutorial](https://www.journaldev.com/1754/strategy-design-pattern-in-java-example-tutorial)

## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
* [Functional Programming in Java: Harnessing the Power of Java 8 Lambda Expressions](http://www.amazon.com/Functional-Programming-Java-Harnessing-Expressions/dp/1937785467/ref=sr_1_1)
