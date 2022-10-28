---
layout: default
title: How to set up autograding
permalink: /autograding.html
---



## Implementation
### Setting up your test file.
Within your template file you will be using for the setup of the students assignment repositories you will need to create some specific files inside here.
In the example where you will not be hiding the answers from your students you can simply create a test file.

Important notes:
Files that you wish to use in order to run tests MUST begin with the name "test_". For example "test_grading.py".
Functions that you use to test assertions must also begin with "test_". For example:
```python
def test_assertions(variable):
	assert variable == True
```
### Calling your test file:
On the final page of creating your assignment click "add test", then "run Python".

<img src="assets\images\Autograding_Initial.PNG" width=300px >

You can then fill in the name of your test(which is usually helpful to name as the same as your actual test file). You can also fill out the commands that you want the test case runner to execute, in this example we have added numpy to illustrate how you would import packages to be used automatically in testing.
Below that you can simply add the filename of the test along with pytest in order to run the file.

<img src="assets\images\Autograding_Details" width=300px >


### How to construct your own testing enviroment.

I will outline a simple instance of a test file you can create here:

Create two files:

- one named "test_grading.py", then one named "student_answers.py"

test_grading.py:

```python

from student_answers import question_1  #Imports the question to be tested from the students file
  
def test_runner():  #Defines our test runner 
   assert question_1() == 40, f"40 expected, System recieved: {question_1()}" # Checks if the assertion is true or false.
  
if __name__ == "__main__":  
   test_runner()

```

student_answers.py:
```python
def question_1(): # Write a function that will return the number 40.  
    number = 40 # Leave this line blank for the student template 
    return number #Returns this number for the student
```


As you can see here this is a simple solution, but it gives an idea how to make some tests.
More complex and robust testing can be achieved, including using secret files so students cannot see answers to tests, as well as a custom autograder we have produced, with more fully featured automatic feedback for the student. 
Work on this is being finalized and will soon be available from the TCSAI github. 

**Link will be here in future**

