# ECE444Lab5

This repo is a copy of https://github.com/mjhea0/flaskr-tdd#deployment

It is done as an exercise for "Lab5" of the course "ECE444" at the University of Toronto

## What are the pros and cons of test driven development?

### **Pros:**
Test driven development (TDD) is a powerful way to force yourself to write quality code. Writing the test cases before writing the code itself means you are essentially defining your requirements. The classic example or most relevant one in our case is tests which define the behaviour and fields of an HTTP API. Which fields should we expect? What is and isn't allowed? These are the kinds of things TDD force you to define, and often, will force you to consider corner cases and what those corner cases represent with respect to business logic. E.g is this corner case even possible? What does this corner case represent in the real world? The concept of defining requirements via tests is not limited to APIs obviously, TDD is usedful to express the relationships between different classes and objects in a general sense, what methods are responsible for what and what should different pieces of the code expect from each other.

Another advantage of TDD is it eases the consequences of leaving projects for some time & return at a later date. Undocumented, untested code is difficult to make sense of. Tests provide you A. a summary of what each module is responsible for and B. a guard rail for further development, if you break something as you are remembering the code you will find out about it through the tests. Of course this scenario is exaggerated, you don't need to forget the codebase for tests to be useful. Regression testing always protects you from breaking core functionality each time you make a change in general.

Finally you can write code faster. Specifically, once the test case has been written it often becomes more clear how the functions / modules should be designed. 

### **Cons:**
Although writing the code becomes faster, the development life cycle itself becomes longer since you have to spend the time translating requirements into test cases. This is certainly not needed when writing quick one off scripts.

Another con is maintaining tests in general, redesign happens & sometimes tests breaking are expected. However if a project is quite old and there are some old tests which break, it can require a more experienced developer to identify the issues & if this is a genuine cause of conern or if it is an expected outcome due to a redesign of the codebase.

Another point to make isn't necessarily a con, but more of a limitation. Some libraries or frameworks you use in your code may simply not be compatible with the kind of test that you are writing. It may be impossible to make the assertions you want to make due to a lack of information, or the ability to gather that information, due to limitations in the libraries. Usually large libraries & frameworks with dedicated communities will provide some form of documentation and support for testing though.

Finally, again not a con per say, but it is easy to fool yourself into a sense of security when writing tests without covering all test cases. The code may seem to pass, but it does not neccessarily cover all corner cases. You can never have "complete test coverage" using _only_ the code. Comprehensive test coverage requires deep domain knowledge on the business logic which can be hard to acquire or even worse, undefined.
