---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/software-eng-principles/revision/l14-testing/"}
---

Testing is big important !
Don’t release with bugs !
![Pasted image 20250112194442.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/Pasted%20image%2020250112194442.png)
Test after every build !

#### Test-Driven Development
This is the idea of creating the tests *before* you create the code. You develop code incrementally, along with a test for that increment. You don’t move on to the next increment until the code that you have developed passes its test. TDD was introduced as part of agile methods such as Extreme Programming.
![Pasted image 20250112194738.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/Pasted%20image%2020250112194738.png)
**Benefits**:
- **Code coverage** - Every code segment has at least one associated test
- **Regression testing** - A regression test suite is developed as a program is developed
- **Simplified debugging** - When a test fails, it should be obvious where the problem lies
- **System documentation** - The tests themselves are a form of documentation
#### Unit Testing
Unit testing is the process of testing individual components **in isolation**.
Units may be:
- Individual functions or methods within an object
- Object classes with several attributes and methods
- Components with defined interfaces used to access their functionality
**Automated Unit Testing**
Whenever possible, unit testing should be automated so that tests are run and checked without manual intervention. In automated unit testing, you make use of a test automation framework (such as JUnit) to write and run your program tests.
Unit testing frameworks provide generic test classes that you extend to create specific test cases. They can then run all of the tests that you have implemented and report, often through some GUI, on the success or failure of the tests.


#### An Input-Output Model of Testing
![Pasted image 20250112200140.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/Pasted%20image%2020250112200140.png)
There are two types of testing:
- **Verification** - Testing expected values and verifying the program actually works
- **Defect Detection** - Testing obscure and devious values to detect bugs
#### The Trade-off Triangle

Yeah!

Also, it’s (much?) more expensive to fix a defect after deploying the program.
There will always be bugs in software, just keep testing till you get bored basically? (or you reach the estimated number of bugs?)

#### Regression Testing
Ensuring that *modifying/updating* a program doesn’t break any previous (maybe unrelated) tests that *were* passed earlier
Basically just re-run all the tests that the program previously passed to make sure they all still pass
