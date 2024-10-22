# Lab-1-Writing-Codes
Q1:

# Question 1
# Make a function that inputs a float greater then one and generates a random number between 1 and the input number.
# If the input is less then 1 then return a 0.
# You can import the library “random” for this


import random
def random_float(x):
if x > 1:
return random.uniform(1,x)
else:
return 0
print(random_float(5))
print(random_float(1))
print(random_float(0.5))
Q2: 
def ComDenom(x):
l = []
for i in range(1,x+1):
if x % i == 0:
l.append(i)
return l
while True:
try:
user_input = int(input("Enter an number: "))
break
except ValueError:
print("Invalid input.Please enter a number.")
print(ComDenom(user_input))
Q3:
def categorize_files(file_list):
"""categorizes files by their file types.
Args:
file_list: A list of names of files.
Returns:
A dictonary where keys are file types and values are lists of files with that type.
"""
file_types = {}
for file in file_list:
file_type = file.split('.')[-1].lower()
if file_type not in file_types:
file_types[file_type] = []
file_types[file_type].append(file.split('.')[0])
return file_types
Downloads = ['run.exe', 'look_at_this_graph.png', 'something_or_other.docx', 'new_folder(4)', 'CRP.pdf', 'not_a_viris.exe', 'homework', 'copy_of_id.png', 'backup.exe']
categorized_files = categorize_files(Downloads)
print(categorized_files)
Q4:
while True:
feeling = input("SHOUT OUT HOW YOU ARE FEELING!!: ")
if feeling.isupper():
print("Alright, i hear you!!")
break
else:
print("What?? SPEAK UP!!")
