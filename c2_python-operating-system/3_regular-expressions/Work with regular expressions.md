## Work with regular expressions
## Graded Quiz. • 50 min
<br>


This graded quiz assesses your understanding of the concepts and procedures covered in the module and lab you just completed. Please answer the questions based on what you learned from the module and the activities you performed in the lab. Questions 1-5 are based on the module. Questions 6-10 are based on the lab. 

Note:

 You can refer to your completed lab for help with the quiz.

 In order to complete this quiz, you must have completed the lab before it.
<br>

Question 1
1. What is a regular expression? 

* A method of encrypting data
* **A sequence of characters that forms a search pattern**
* A type of data structure in Python
* A function in Python for handling exceptions
<br>
Question 2
In regular expressions, what does the re.split() function do? 

* Checks if a string contains a specific substring or not 
* Removes all occurrences of a specified substring from a string
* **Splits a string into a list of substrings based on a regular expression pattern**
* Concatenates multiple strings into one string
<br>

3. You have a list of website urls that includes both securely encrypted websites that begin with https:// and the unencrypted websites that begin with http://. The list includes websites that end in .com and .co. 

Complete the secure_website_domain function so it returns the part of the website between www. and the last part of the url (.com or .co) for only the secure websites.

def secure_website_domain(website):
 pattern = r"^https:\/\/www\.(.*)\.(com|co)$" # enter the regex pattern here
 result = re.search(pattern, website) # enter the re method here
 if result is None:
  return ""
 return result.group(1)# enter the correct capturing group


print(secure_website_domain("http://www.text.com")) #Should return nothing
print(secure_website_domain("https://www.text.com")) #Should return text
print(secure_website_domain("http://www.text.co")) #Should return nothing
print(secure_website_domain("https://www.text.co")) #Should return text

<br>
4. You are exploring the punctuation at the end of sentences and want to split sentences so that each word is separate and any punctuation is included in the word next to it. Complete the parse_sentences function to accomplish this task. 

def parse_sentences(sentence):
 pattern =r'\b\w+\b[.!?]*|\+' #enter the regex pattern here
 result = re.findall(pattern, sentence) #enter the re method  here
 return result

print(parse_sentences("Hello! How are you doing?")) # should return ['Hello!', 'How', 'are', 'you', 'doing?']
print(parse_sentences("what a beautiful day it is")) # should return ['what', 'a', 'beautiful', 'day', 'it', 'is']
print(parse_sentences("2 + 2 is definitely 4!")) # should return ['2', '+', '2', 'is', 'definitely', '4!']

<br>
5. A company uses Product ID numbers to identify each product line it makes. Each product ID starts with 4 digits, followed by a hyphen (-), followed by two capital letters, followed by a hyphen (-), followed by two more digits, in the format 1234-AB-12. The manufacturing team records information about the production of each product line daily. 

You want to extract the product ID numbers of one of these product lines, which begins with a 1. The other characters in the product ID can be any digit or variable, as long as they follow the product ID format described above. Complete the following code so the find_productID function returns all product ID numbers that match the product of interest. 

def find_productID(report):
  pattern = r'1\d{3}-[A-Z]{2}-\d{2}'#enter the regex pattern here
  result = re.findall(pattern, report) #enter the re method  here
  return result
  
print(find_productID("Products 1234-AB-30 and 2234-AB-30, not items 12-AB-30 or 12345-AB-30")) # Should return ['1234-AB-30']
print(find_productID("Products of interest are 1234-AB-30, 1678-XZ-11, and 1561-CD-57. We're not interested in other products like 2345-AB-29.")) # Should return ['1234-AB-30', '1678-XZ-11', '1561-CD-57']
<br>
6. In the lab, you defined the replace_domain as: 
   def replace_domain(address, old_domain, new_domain):
  old_domain_pattern = r'' + old_domain + '$'
  address = re.sub(old_domain_pattern, new_domain, address)
  return address

In the lab, you defined the replace_domain as: 

4123
def replace_domain(address, old_domain, new_domain):
  old_domain_pattern = r'' + old_domain + '$'
  address = re.sub(old_domain_pattern, new_domain, address)
  return address
What role does this function have in the process of updating outdated domain names with new domain names?

* **To replace the old domain with the new domain in an email address**
* To write the updated list to a CSV file
* To read data from a CSV file
* To iterate over a list of email addresses

In the lab, you were tasked with initializing a list called old_domain_email_list and populating it with email addresses that contain the old domain name and meet the criteria defined in the contains_domain function. The list of current email addresses was provided in the list user_email_list.  How did you accomplish this in the lab?

* Step 1: Manually inspected each email address in the user_email_list. Step 2: Appended email addresses with the old domain to the old_domain_email_list.


* Step 1: Used a list comprehension to extract all email addresses from the 
  user_email_list that match the old domain pattern. Step 2: Appended email addresses with the old domain to the old_domain_email_list. 


* Step 1: Initialized old_domain_email_list with an empty list. Step 2: Used a regular expression to find all email addresses in the user_email_list that match the old domain pattern. Step 3: Appended email addresses with the old domain to the old_domain_email_list. 


* **Step 1: Initialized old_domain_email_list with an empty list. Step 2: Used a for loop to iterate over the emails in user_email_list, checking each email address to determine if it contains the old domain using the contains_domain function, which uses regex to check if it matches the old domain. Step 3: Appended email addresses with the old domain to the old_domain_email_list.** 

<br>

8. Why is it important to write the list to an output file in a Python script, as specified by the variable report_file?

* The output file serves as a backup for the original data, preventing any loss of information in case of script errors.
* Writing to an output file allows for temporary storage of data, which is essential for debugging the script.
* **Writing the updated list to an output file provides a permanent record of the changes made, allowing for data preservation and further analysis.**
* Writing to an output file is a required step in Python programming for all data manipulation tasks to ensure memory efficiency.

<br>

9. Which Python libraries or modules are commonly employed to perform updates to domain names to a new specified domain and saving all the modified domain names to a separate file?

* os and sys
* **re (regular expressions) and open() function**
* pandas and numpy
* re (regular expressions) and requests
<br>

10. Question 10
In the process of updating email domains in a CSV file using Python, how do the contains_domain and replace_domain functions work together?

* contains_domain deletes email addresses with outdated domains, and replace_domain creates new email addresses from scratch.
* **contains_domain uses a regular expression to identify emails with a specific domain, and replace_domain replaces these domains with new ones.**
* contains_domain sorts the email addresses, and replace_domain reverses their order.
* contains_domain encrypts the email addresses, and replace_domain decrypts them back to their original form.