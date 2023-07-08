# SOLID Principles
SOLID is a mnemonic for five design principles intended to
make software designs more understandable, flexible and
maintainable.

## Single responsibility principle
There should be only one reason to change the body of a class.
  Make a lot of classes that every one of them is responsible only for one functionality. Imagine that you've working on a project for many years. Now you want to review a class which is created 4 years ago and it has a lots of lines of code and functionalities and it's too hard to scan through whole code and undrestand it completely.
  There is also another problem. If your class does many things you have to change it everytime one of these things changes and there is a high probability to break other parts of the class that are not supposed to change.

  Let's consider an example. We have a Employee class which has two methods; one for getting employee's name and one for printing time sheet report. These are two funciontality so the Employee class should be changed if 1.We need to modify Employee's fields. 2.The format of timesheet has been changed. So it contradicts this principle.
![image](https://github.com/Peyman-hme/BasicsOfOOP/assets/62210041/4f0629be-b6bc-4526-b0f5-7b2b97f17823)

  Now we want to solve this problem by extracting out printing timesheet functionality from this class and implement it in a new class and make a association relationship between Employee class and this new class.

![image](https://github.com/Peyman-hme/BasicsOfOOP/assets/62210041/e2031a99-c873-4c6e-bb5f-de7f721b7deb)



