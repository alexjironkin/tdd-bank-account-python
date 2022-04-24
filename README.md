[![Build and Test](https://github.com/alexjironkin/tdd-bank-account-python/actions/workflows/build_and_test.yml/badge.svg?branch=main)](https://github.com/alexjironkin/tdd-bank-account-python/actions/workflows/build_and_test.yml)

# Driving out a Bank Account with TDD

This session will be fun. That's the primary objective, have fun and code. That's it! In this session we will talk for a little bit about why XP practices are important and then we can write some code practicing two of the most fundamental ones.

The code will be super easy, this is not about writing complicated code, quite the opposite. We will get pairs of you to build really simple test driven code. It will make you rethink how you write code. For those of you after more of a challenge, we have included some optional Object Oriented (calisthenics) rules to apply.

Come in pairs or make new friends on the day. Please all **bring your own laptop** with your favourite IDE installed.

Two key things to learn / practice in this Kata:

1. Test Driven Development
2. Pair programming

# Instructions

1. Clone the repository with the following command.

   `git clone https://github.com/xp-dojo/tdd-bank-account-python`

   If you have problems with SSL, you can try the following.

   `git clone -c http.sslVerify=false https://github.com/xp-dojo/tdd-bank-account-python`

   If you have problems with a proxy, you can `unset http_proxy` and `unset https_proxy` (or equivalent for your OS).

2. Install python dependencies:
   `pip install -r requirements.txt`
3. Open the project from your IDE, and you will find **tdd_bank_dojo** source folder with **tests** and **account.py**. Instructions for setting up VS Code can be found [here](vscode.md).
4. Run your tests:
   `python -m pytest tdd_bank_dojo/tests`
5. Implement the following user requirements in a TDD fashion. Work in pairs and read the guidelines and background information below before starting.

## User Requirements

1.  I can **Deposit** money to accounts
2.  I can **Withdraw** money from accounts
3.  I can **Transfer** amounts between accounts (if I have the funds)
4.  I can print out an Account balance slip (date, time, balance)
5.  I can print a statement of account activity (statement)
6.  I can apply Statement filters (include just deposits, withdrawal, date)

# Guidelines and Background

## Test Driven Development

Test driven development is based on the principles of test-first development (where you write the test first) but goes an extra step to actually driving the code using the IDE. The basic cycle follows the **<span style="color: red;">Red</span> -> <span style="color: green;">Green</span> -> <span style="color: blue;">Refactor</span>** model:

- **Red**: write a failing test. Write a test that describes (think documentation) what the function you are writing actually does. Likely this will not even compile (this is fine, not compiling IS a failing test).
- **Green**: now write enough of an implementation to make the test pass. You should write the simplest code possible to make the code pass and resist the urge to write more than is actually needed. Consider the [YAGNI](https://martinfowler.com/bliki/Yagni.html) principle.
- **Refactor**: now we re-read the code and make sure that this is good enough to push to the _world at large_. You should ask yourself at this point how the next person that reads this code will experience it.

![](rgr.jpg)

As a walkthrough consider applying TDD as a two stage process, the first phase writes the API in the test **as it should be** (write the code you would like someone else to have written for you). In this case the compiler _IS_ the failing test, you rewrite it until you are happy and then to make it go green you use the IDE to create the classes and methods as per the test (dont type them, let the IDE do the work). The next phase of the cycle implements the methods to get the unit tests passing, followed by the refactoring to complete the RGR cycle described above.

## Pair Programming

There are many different ways to do pair programming, the most common model is the Driver-Navigator model. For this kata, try and follow as below for simplicity. There are two roles in this model (you should switch often to keep it interesting):

- **The Driver** is the person wiring the code (test driven) and implementing. The Driver should be explaining what they are doing in a running monologue so the Navigator understands the direction taken and can assess it (also it keeps the Navigator engaged).
- **The Navigator** is the person observing and thinking about the big picture. The best Navigators are those that ask **why?** often to check that we **build the right thing, and build the thing right**. For this kata, the Navigator is checking that they are really test driving (using the IDE) and that the code **does what it says and says what it does**. When applying object calisthenics the Navigator should be checking that the Nine rules are not being broken. Correction and learning is the key here.

## Object Calisthenics

Object calisthenics are a set of rules or constraints designed to challenge and stretch yourself when applied to OO coding. For an extra challenge when implementing the user requirements, consider applying rules below.

### The Rules (bold ones are MUST)

1. **Don’t use the `else` keyword**
2. **Wrap all primitives and strings (in an object)**
3. **No properties**
4. **First class collections**
5. Use only one dot per line
6. Don’t abbreviate
7. Keep all entities small (50 lines)
8. No classes with more than two instance variables
9. Reduce boilerplate code in your tests by using fixtures

See the links below for more details.

# Additional Information

- Project based on the original from Sandro Mancuso and the LSCC
- Original idea for the kata: [How Object-Oriented Are You Feeling Today?](https://www.slideshare.net/KrzysztofJelski/how-object-oriented-are-you-feeling-today) - Krzysztof Jelski (Session on the Software Craftsmanship UK 2011 conference)
- [Object Calisthenics pdf](http://www.cs.helsinki.fi/u/luontola/tdd-2009/ext/ObjectCalisthenics.pdf)
- Object Calisthenics (full book), Jeff Bay in: The ThoughtWorks Anthology. Pragmatic Bookshelf 2008

# License

The content of this project (educational material, slides and alike) are licensed under the Creative Commons Attribution Share Alike 4.0 International (CC-BY-SA) license, whilst the underlying source code used to support the educational material is licensed under the Apache 2.0 license.
