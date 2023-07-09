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


## Open/Close principle
Classes should be open for extension but closed for
modification.
This principle is about adding new feature without breaking the existing code. A class is open whrn you can extend it. Create new subclasses and mew features, methods, etc. Howeever some classes are final. This means that this class is unable to be extended. We call these classes as complete.
When a code is developed, tested and reviewed, changing its body is risky. Instead of changing a part of the code directly, you can simply create a subclass and override that part of the main code which you want to behave differently. This solution offers adding new feature without breaking the existing code.
Let's consider an example. You have a Order class which it has a getShippingCost method that vase on type of the shipping field in the instance of class, calculate its cost. Now imagine that you want to add a new shipping type into your program, you have to change the body of getShippingCost method to add a new "else-if" clause for calculating the new type of shipping. So you contradict the open/close principle and you break a existing code.
![image](https://github.com/Peyman-hme/BasicsOfOOP/assets/62210041/7d3c4a40-03ba-4477-a236-2786ddda2444)


The solution of this problem is creating a new interface which is called Shipping. Then create some classes for every type of shipping. They implement Shipping interface. Now we can write getShippingCost in Order class in order to calling getCost method on shipping instance.

![image](https://github.com/Peyman-hme/BasicsOfOOP/assets/62210041/f26ba065-3e6a-44f7-a0d8-beb36d04072d)

Now if you want to add a new shipping type you can simply create a new class and implement Shipping interface without breaking existing code.



