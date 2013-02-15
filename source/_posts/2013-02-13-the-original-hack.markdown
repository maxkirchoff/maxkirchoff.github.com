---
author: max
layout: post
title: The Original Hack - "!!"
date: 2013-02-12 14:06
comments: true
categories: 
- Hack
- Philosophy
- Logic
- Math
- Negation
- Programming
- PHP
- Javascript
- Ruby
- Python

---
 
Metaphysical nihilism is a funny thing. Most major philosophical and religious doctrine revoke non-existence as a "non quality" of both the material and immaterial worlds. Non-existence is not a logical case that can be validated. In other words, one cannot say "there is not" without referencing a subject. `!` `¬` or `~` (all roughly symbolizing negation or NOT-ness) require application to a subject. However, in defining an argument to metaphysical nihilism, we inherently say that no subject exists - thus undermining the basic operation.

None of this is new thinking. It's been around forever and philosophers have beaten each other up for it in every age. 
The [Monists](http://en.wikipedia.org/wiki/Monism) set up a reality where all substances can be reduced to one substance. This reality became the foundation for 
[Gorgias](http://en.wikipedia.org/wiki/Gorgias), an early thinker dealing with "non-existence", to reduce that single, immutable substance to a non-substance or nothingness. 

> (1)Nothing exists, or (2)if it does exist we cannot know it, or (3)if we can know it it is impossible to communicate it.

Convincing right? Yea, didn't think so.
So what's wrong with the above thought? Let's try to rewrite it in python:

####Proposition 1

```
! # there is NOT
```
**ERROR!**

####Proposition 2 & 3

```
if !!
	print !! # if there's NOT NOT, then we can print it
```
**ERROR!**

So, python doesn't get us anywhere. Neither will Javascript, Ruby or PHP. Hell, symbolic logic and math will fail us as well.
Why?

## The dependencies of logic
Logic has few dependencies, but they are **hugely important** and are the basis of every language (natural or otherwise). 

* **Operators are universally the same** *(i.e. AND, OR, NOT always act the same)*
* **a given State is universally the same** *(TRUE is always TRUE)*

With the above dependencies met, we can use logic with the basic states of TRUE AND FALSE.

`IF TRUE THEN TRUE`

`IF NOT TRUE THEN FALSE`

`IF FALSE AND NOT TRUE THEN FALSE`

Everything is beautiful… and then… 

## The rise of the NOTHING thing
So, logic evaluates operators and conditions of statements to determine TRUE/FALSE states. When language developed, shortcomings of logic became apparent. While logic relied on immutable states, we observed a another mode or state that was changing, a basic representation being existence/nonexistence. A thing may "be" and then "not be" or vice-versa, or any sort chain of be/not/be/not/be/not states.  

Linguistically we adopted this status and formed the sentiments of existence/nonexistence all while an argument arose that continues today over the objective nature of state change in the universe. (See [Heraclitus](http://en.wikipedia.org/wiki/Heraclitus) and [Parmenides](http://en.wikipedia.org/wiki/Parmenides))

The language constructs developed underneath previous logical operations to convey this sub-logical mode of not yet being defined or "existing".

Commonly this is called *nothingness*, *non-existence*, etc.

In programming this is expressed as *undefined*, *null*, *nil*, *None*

In practice, the mode seems helpful as it allows the expression of a state that cannot have logical conditions or operations applied to it.

```
Me: Where is my hat, Christina?
Christina: Max, you don't own a hat.
Me: Oh, okay.
```

or expressed in ruby

```
if defined? max_hat				 # does max have a hat
	return location(max_hat)		# get the hat's location
else								# otherwise
	return "you don't own a hat!"	# tell him he doesn't own a hat

```

It may seem that `defined?`, `nil?`, `isset()` and other sorts of methods in programming are just more advanced operators, but they are not. They are checks that apply to a sub-logic state, the state of existence.

## Hacking (Non)Existence
However, in common practice in programming, math, philosophy (etc) we find ourselves with logical conditions and operators beginning to mix into a sub-logical mode. It's not clear when or how we began this concoction of mis-matched expressions, but it has been around as long as we can remember. A good way to examine this use of disperate items is in code:


```
> nonexistence = nil	# So nonexistence doesn't exist

> puts nonexistence		# Printing nonexistence gives us nothing. cool.

> puts !nonexistence 	# Printing the "not nonexistence"
true					# gives us something…and it's true. ok, i guess.

> puts !!nonexistence	# Printing the "not not nonexistence"
false					# gives us something…and it's false. wat?
```

And this is where Gorgias (and many others included the [Sophists](http://en.wikipedia.org/wiki/Sophist)) found their footing. If you apply the pre-logical constructs of existence within the conditionals of logic…everything falls apart. Logic validates existing statements, but we find ourselves with validation of a non-existent mode. WTF?

It's a hack, a really old hack, possibly the first hack.

Somehow we went from ordered operators and conditions, to a disordered reality of invalid universal states. If !!nonexistence can be false (signifying inherent existence) then nonexistence itself exists. 

Seriously, WTF?

We are left to wonder then, if logic can be hacked, can it be broken?




