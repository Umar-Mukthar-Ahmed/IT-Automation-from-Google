Question 1
In the Implementing Unit Testing lab, you navigated to a data directory and a scripts directory. What did the commands to navigate to these directories begin with?

1 point

nano ~/scripts/emails_test.py 


cd ~/


ls 


cat

2.
Question 2
When you looked for the script emails.py in the scripts directory, what command did you use to navigate to the scripts directory? 

1 point

cd ~/scripts


nano ~/scripts/emails_test.py 


ls user_emails.csv


cat emails.py

3.
Question 3
There are plenty of practical reasons for writing a test case for a script. From a developer’s perspective, what is a good reason to write test cases for your scripts? 

1 point

Writing a test makes developers examine the script’s design, leading you to create better scripts in the future. 


Scripts will work on updated platforms as long as tests are used. 


Writing a test enables developers to write longer code. 


Writing a test ensures a developer’s code will be bug free. . 

4.
Question 4
Which of the following statements accurately describe how try/except blocks work? Select all that apply.

1 point

If an exception occurs during the execution of the try clause, the try clause is executed and ignored.


If no exceptions occur, the try clause is ignored.


If an exception occurs during the execution of the try clause, the rest of the try clause is then skipped.


The try clause is executed.

5.
Question 5
When testing a working script with a known bug, what is the first step in the testing process? 

1 point

Find all bugs in the software.


Reproduce the bug. 


Use the software so that it works correctly


Create a list of features that are unnecessary. 

6.
Question 6
When referring to unit testing, what are “classes”? 

1 point

Classes are test cases that correct bugs.


Classes allow Python files to access scripts from another Python file.


Classes bundle data and functionality together. 


Classes are individual units of testing that checks for a specific response to inputs. 

7.
Question 7
The following code will either return an email address for an employee or an error message if there is no employee matching the name entered. What would the error message be?

if email_dict.get(fullname.lower()):
    return email_dict.get(fullname.lower())
else:
    return "No email"

1 point

“No email address found”


“Missing parameters”


“No employee found”


“No email”

8.
Question 8
Which of the following is the correct order of blocks in a try/except construct? 

1 point

try, raise, except, finally


try, except, finally, raise


raise, try, except, finally


try, except, raise, finally

9.
Question 9
The following import statement allows a Python file to access the script from another Python file. What exactly will this statement cause to be imported? 

	from emails import find_email

1 point

It imports the function emails.py, which is defined in the script find_email.


It imports the script find_email, which is defined in the function emails.py.


It imports the emails listed in the script find_email.


It imports the function find_email, which is defined in the script emails.py.

10.
Question 10
When writing a try/except clause, how many except clauses can be included? 

1 point

One more except clauses than there are specific handlers for different exceptions.


Only one.


As many except clauses are needed to specify handlers for different exceptions. 


As many as needed as long as there is one try clause per except clause. 