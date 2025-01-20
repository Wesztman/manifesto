_A couple of things to think about when working with code._

## **Look at your code through the eyes of your users/customer.**

Always question the usefulness of the code you deliver. Try to imagine you´re the user of the library your writing. Would you be happy to use the functions you provide? Is it understandable? Internal customers are also customers.

## **Every row of code should have a purpose.**

Don't assign stuff to unecessary local variables or push dead code. **Always** review your own pull requests before publishing, ask yourself if every line of code is needed and why. 

And remember that it is always you that is responsible for the code you provide in a PR.

## **Always question other developers code.**

It´s easy to think that whatever any senior developer write is correct. You should always question other peoples code, they also make stupid mistakes, the same as you, don't copy anything blindly.

## **Favor readability over fancy functionality.**

Code that is easy to understand will save your team great headaches down the line. Try to resist the urge to look cool with fancy functionality if you don't have a good reason for it. 

Keep your PR:s small, one feature, one PR.

And no [magic numbers](https://en.wikipedia.org/wiki/Magic_number_(programming)) please... we have enums and named tuples for that.

[KISS](https://en.wikipedia.org/wiki/KISS_principle)

## Code always comes with tests.

Well at least most of the time...

In the majority of cases there is no reason to not provide any kind of tests to your code. 

Sure, if you´re in a complex code base where there has been no thoughts on unit testing from the beginning I can forgive you.

Code pushed to repositories with an already established test suite should **always** have tests added, no excuses.
