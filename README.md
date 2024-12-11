# Practical_4
Practical_4

File: /home/ubuntu/practical4dsl.py Page 1 of 3
'''Experiment Number 5: Write a python program to store first year percentage of students
in an array.
Write function for sorting array of floating point numbers in
ascending order using:
a) Selection Sort
b) Bubble Sort and display top five scores
'''
# Function for Selection Sort of elements
def Selection_Sort(marks):
for i in range(len(marks)):
# Find the minimum element in remaining unsorted array
min_idx = i
for j in range(i + 1, len(marks)):
if marks[min_idx] > marks[j]:
min_idx = j
# Swap the minimum element with the first element
marks[i], marks[min_idx] = marks[min_idx], marks[i]
print("Marks of students after performing Selection Sort on the list : ")
for i in range(len(marks)):
print(marks[i])
#<--------------------------------------------------------------------------------------->
# Function for Bubble Sort of elements
def Bubble_Sort(marks):
n = len(marks)
# Traverse through all array elements
for i in range(n - 1):
# Last i elements are already in place
for j in range(0, n - i - 1):
# Traverse the array from 0 to n-i-1
# Swap if the element found is greater than the next element
if marks[j] > marks[j + 1]:
marks[j], marks[j + 1] = marks[j + 1], marks[j]
print("Marks of students after performing Bubble Sort on the list :")
for i in range(len(marks)):
print(marks[i])
#<--------------------------------------------------------------------------------------->
# Function for displaying top five marks
def top_five_marks(marks):
print("Top",len(marks),"Marks are : ")
print(*marks[::-1], sep="\n")
#<----------------------------------------------------------------------------------------
>
# Main
marks=[]
n = int(input("Enter number of students whose marks are to be displayed : "))
print("Enter marks for",n,"students (Press ENTER after every students marks): ")
for i in range(0, n):
ele = int(input())
marks.append(ele) # adding the element
File: /home/ubuntu/practical4dsl.py Page 2 of 3
print("The marks of",n,"students are : ")
print(marks)
flag=1;
while flag==1:
print("\n---------------MENU---------------")
print("1. Selection Sort of the marks")
print("2. Bubble Sort of the marks")
print("3. Exit")
ch=int(input("\n\nEnter your choice (from 1 to 3) : "))
if ch==1:
Selection_Sort(marks)
a=input("\nDo you want to display top marks from the list (yes/no) : ")
if a=='yes':
top_five_marks(marks)
else:
print("\nThanks for using this program!")
flag=0
elif ch==2:
Bubble_Sort(marks)
a = input("\nDo you want to display top five marks from the list (yes/no) : ")
if a == 'yes':
top_five_marks(marks)
else:
print("\nThanks for using this program!")
flag = 0
elif ch==3:
print("\nThanks for using this program!!")
flag=0
else:
print("\nEnter a valid choice!!")
print("\nThanks for using this program!!")
flag=0
#<----------------------------------------END OF
PROGRAM------------------------------------------------->
####################################################################################
Output : -
ubuntu@ubuntu-Vostro-460:~/DSL$ /bin/python3 /home/ubuntu/DSL/Practical5.py
Enter number of students whose marks are to be displayed : 6
Enter marks for 6 students (Press ENTER after every students marks):
79
63
59
91
88
77
The marks of 6 students are :
[79, 63, 59, 91, 88, 77]
---------------MENU---------------
1. Selection Sort of the marks
2. Bubble Sort of the marks
3. Exit
File: /home/ubuntu/practical4dsl.py Page 3 of 3
Enter your choice (from 1 to 3) : 1
Marks of students after performing Selection Sort on the list :
59
63
77
79
88
91
Do you want to display top marks from the list (yes/no) : yes
Top 6 Marks are :
91
88
79
77
63
59
---------------MENU---------------
1. Selection Sort of the marks
2. Bubble Sort of the marks
3. Exit
Enter your choice (from 1 to 3) : 2
Marks of students after performing Bubble Sort on the list :
59
63
77
79
88
91
Do you want to display top five marks from the list (yes/no) : yes
Top 6 Marks are :
91
88
79
77
63
59
---------------MENU---------------
1. Selection Sort of the marks
2. Bubble Sort of the marks
3. Exit
Enter your choice (from 1 to 3) : 3
Thanks for using this program!!
