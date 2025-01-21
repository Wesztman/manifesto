_A couple of things to think about when working with code._

## Look at your code through the eyes of your users/customer.

Always question the usefulness of the code you deliver. Try to imagine you´re the user of the library/app/other your writing. Would you be happy to use the functions you provide? Is it understandable? Internal customers are also customers.

## Every row of code should have a purpose.

Don't assign stuff to unecessary local variables or push dead code. **Always** review your own pull requests before publishing, ask yourself if every line of code is needed and why. 

And remember that it is always you that is responsible for the code you provide in a PR.

## Always question other developers code.

It´s easy to think that whatever any senior developer write is correct. You should always question other peoples code, they also make stupid mistakes, the same as you, don't copy anything blindly.

## Favor readability over fancy functionality.

Code that is easy to understand will save your team great headaches down the line. Try to resist the urge to look cool with fancy functionality if you don't have a good reason for it. 

Keep your PR:s small, one feature, one PR.

And no [magic numbers](https://en.wikipedia.org/wiki/Magic_number_(programming)) please... we have enums and named tuples for that.

[KISS](https://en.wikipedia.org/wiki/KISS_principle)

## Code always comes with tests.

Well at least most of the time...

In the majority of cases there is no reason to not provide any kind of tests to your code. 

Sure, if you´re in a complex code base where there has been no thoughts on unit testing from the beginning I can forgive you.

Code pushed to repositories with an already established test suite should **always** have tests added, no excuses.

And remember to always add tests to cover bugs which are discovered after release, you will release again, you will make the same mistake again.

Blackbox/e2e testing where you input something and check the output makes it much easier to refactor the insides.

Always try to test as much as possible using only software, rigs and hardware requires alot of maintenance and complex versioning.

# Addition based on Matt Rickards brilliant [Reflections on 10,000 Hours of DevOps](https://blog.matt-rickard.com/p/reflections-on-10000-hours-of-devops?utm_campaign=post&utm_medium=web)

_The best bits in my opinion from this splendid list of goodies. Note: I made some additions myself to certain headings._

## Version your APIs, packages and templates, even internal ones

Version your APIs, packages and templates. Even the internal ones. No stupid breaking changes when pushing stuff. Don’t reinvent the wheel. Use semantic versioning. 

This also makes rolling back a broken update so much easier.

## Do not tolerate flaky (randomly failing) tests

Do not tolerate flaky tests. Fix them (or delete them).

A test you cannot trust is of no use and it will end up blocking your PR:s and wasting your time.

## Have a high bar for introducing new dependencies and tools

Have a high bar for introducing new dependencies. Especially ones that require special builds or environments.

It might be tempting, but remember that you could end up needing to all this extra stuff.

Beware toolchain sprawl. Every new tool requires expertise, management, and maintenance.

## Make environments easy to set up from scratch

Make environments easy to set up from scratch. This helps in every stage: local, staging, and production. 

This does not only make it easier to onboard new people to your team. It also makes it easier to automate things overall. 

Having an easy to set up environment means that you can probably do it on the fly at the start of your pipelines. Which means that you do not have to keep tools and libs that needs maintenance installed on your agents/runners, saving you tons of time.

## Avoid shiny objects but know when the paradigm shifts

Especially true with all these new shiny programming languages.

It might not be wise to jump on the train immediately, but also, do not stubbornly get stuck if a change is obviously better for you.

## Default to closed (minimal permissions for) infrastructure.

It might take some extra time to think about who needs access where and implementing authentication. But in the end it could save you from a real security headache.

## Default code and internal docs to open for humans. 

It’s usually a net benefit for developers to view code outside their own project. 

Your co-workers usually don't have any ill intent and if you are worried you should just protect your repos/branches with proper rules, requiring PR:s, which you should always do anyway.

## If you have to do a simple task more than 3 times, automate it.

Just do it.

It might be some work now, but you will thank yourself later.

I'll say it again, just do it.

## Linear git history makes rollbacks easier.

This can be achieved in multiple ways. 

For me this means squashing every PR into one commit onto main. 

Having a main repo where you know that every single commit has been reviewed, tested and runs without issues saves alot of headache.






