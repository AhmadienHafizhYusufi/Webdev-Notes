# Why use it & example

## Why use it

So far all we've discussed just feels like adding restrictions to your code. So
what is the real benefit and why do so many people love using Typescript?
**Because** of the restrictions. Restrictions are **good**. When developing by
yourself- You restrict yourself from using your variables or methods
incorrectly. This means you won't have as many confusing bugs that are hard to
track down. You'll be able to catch these bugs before you even run the code.

What you're really doing is _describing_ your code and how it behaves to the
typescript compiler and your code editor. By learning to describe your code
accurately- you will not only write safer and less buggy code, but you'll become
a **stronger developer**. You'll more clearly understand all code, not just your
own.

The benefits really shine when working in a team. By adding all these types and
'restrictions' to the code you write- you can enforce **how** other people on
your team use your code. If you write a function that explicitly takes a string
as an argument and returns an array- no one on your team will accidentally pass
in a number to the function. And they'll know the return type without even
looking at your code just by hovering over your function they imported.

You'll get access to powerful autocomplete features not only in your own code,
but when using code written by another teammate. You won't need to dig through
their code to figure out what's happening- your code editor will just know. For
example- after defining this **Post** type, when you create an object with that
type then your editor will help you write the rest:
