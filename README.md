L = [11, 12, 13, 14]

# (i) Add 50 and 60 to L
L.append(50)
L.append(60)

# (ii) Remove 11 and 13 from L
L.remove(11)
L.remove(13)

# (iii) Sort L in ascending order
L.sort()

# (iv) Sort L in descending order
L.sort(reverse=True)

# (v) Search for 13 in L
if 13 in L:
    print("13 is present in L")
else:
    print("13 is not present in L")

# (vi) Count the number of elements present in L
count = len(L)
print("Number of elements in L:", count)

# (vii) Sum all the elements in L
sum_all = sum(L)
print("Sum of all elements in L:", sum_all)

# (viii) Sum all ODD numbers in L
sum_odd = sum(num for num in L if num % 2 != 0)
print("Sum of all odd numbers in L:", sum_odd)

# (ix) Sum all EVEN numbers in L
sum_even = sum(num for num in L if num % 2 == 0)
print("Sum of all even numbers in L:", sum_even)

# (x) Sum all PRIME numbers in L
def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

sum_prime = sum(num for num in L if is_prime(num))
print("Sum of all prime numbers in L:", sum_prime)

# (xi) Clear all the elements in L
L.clear()

# (xii) Delete L
del L

# second Question
D = {1: 5.6, 2: 7.8, 3: 6.6, 4: 8.7, 5: 7.7}

# (i) Add new entry in D; key=8 and value is 8.8
D[8] = 8.8

# (ii) Remove key=2 from D
del D[2]

# (iii) Check whether key=6 is present in D
if 6 in D:
    print("Key 6 is present in D")
else:
    print("Key 6 is not present in D")

# (iv) Count the number of elements present in D
count = len(D)
print("Number of elements in D:", count)

# (v) Add all the values present in D
sum_values = sum(D.values())
print("Sum of all values in D:", sum_values)

# (vi) Update the value of key 3 to 7.1
D[3] = 7.1

# (vii) Clear the dictionary
D.clear()

# 3rd question 

S1 = {10, 20, 30, 40, 50, 60}
S2 = {40, 50, 60, 70, 80, 90}

# (i) Add 55 and 66 in Set S1
S1.add(55)
S1.add(66)

# (ii) Remove 10 and 30 from Set S1
S1.remove(10)
S1.remove(30)

# (iii) Check whether 40 is present in S1
if 40 in S1:
    print("40 is present in S1")
else:
    print("40 is not present in S1")

# (iv) Find the union between S1 and S2
union_set = S1.union(S2)
print("Union of S1 and S2:", union_set)

# (v) Find the intersection between S1 and S2
intersection_set = S1.intersection(S2)
print("Intersection of S1 and S2:", intersection_set)

# (vi) Find S1 - S2
difference_set = S1 - S2
print("S1 - S2:", difference_set)

# 4th question

# (i) WAP to print 100 random strings whose length is between 6 and 8:
import random
import string

for _ in range(100):
    length = random.randint(6, 8)
    random_string = ''.join(random.choices(string.ascii_letters, k=length))
    print(random_string)
# (ii) WAP to print all prime numbers between 600 and 800:

lower_limit = 600
upper_limit = 800

for num in range(lower_limit, upper_limit + 1):
    if num > 1:
        for i in range(2, int(num**0.5) + 1):
            if (num % i) == 0:
                break
        else:
            print(num)
# (iii) WAP to print all numbers between 100 and 1000 that are divisible by 7 and 9:
for num in range(100, 1001):
    if num % 7 == 0 and num % 9 == 0:
        print(num)
# 5thquestion
import random

# Create the two lists
list1 = random.sample(range(10, 31), 10)
list2 = random.sample(range(10, 31), 10)

# Print the two lists
print("List 1:", list1)
print("List 2:", list2)

# Find common numbers in the two lists
common_numbers = list(set(list1) & set(list2))
print("Common numbers:", common_numbers)

# Find unique numbers in both lists
unique_numbers = list(set(list1) ^ set(list2))
print("Unique numbers:", unique_numbers)

# Find minimum in both lists
min_number = min(min(list1), min(list2))
print("Minimum number:", min_number)

# Find maximum in both lists
max_number = max(max(list1), max(list2))
print("Maximum number:", max_number)

# Find sum of both lists
sum_of_lists = sum(list1) + sum(list2)
print("Sum of both lists:", sum_of_lists)
# 6th question
import random

# Function to check if a number is prime
def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

# Create the list of 100 random numbers
random_numbers = random.sample(range(100, 901), 100)

# Count and print the odd numbers
odd_numbers = [num for num in random_numbers if num % 2 != 0]
print("Odd numbers:", odd_numbers)
print("Count of odd numbers:", len(odd_numbers))

# Count and print the even numbers
even_numbers = [num for num in random_numbers if num % 2 == 0]
print("Even numbers:", even_numbers)
print("Count of even numbers:", len(even_numbers))

# Count and print the prime numbers
prime_numbers = [num for num in random_numbers if is_prime(num)]
print("Prime numbers:", prime_numbers)
print("Count of prime numbers:", len(prime_numbers))

# 7th

D = {1: "One", 2: "Two", 3: "Three", 4: "Four", 5: "Five"}

# Open the file in write mode
with open("output.txt", "w") as file:
    # Iterate over the dictionary items
    for key, value in D.items():
        # Write the key-value pair to the file
        file.write(f"{key}, {value}\n")

print("Data written to the file successfully.")

# 8th question

L = ["One", "Two", "Three", "Four", "Five"]

# Open the file in write mode
with open("output.txt", "w") as file:
    # Iterate over the elements in the list
    for element in L:
        # Calculate the length of the element
        length = len(element)
        # Write the element and its length to the file
        file.write(f"{element}, {length}\n")

print("Data written to the file successfully.")

# 9th 10th and 11th question
import random
import string

# Open the file in write mode
with open("random_strings.txt", "w") as file:
    # Generate and write 100 random strings to the file
    for _ in range(100):
        length = random.randint(10, 15)
        random_string = ''.join(random.choices(string.ascii_letters + string.digits, k=length))
        file.write(random_string + "\n")

print("Random strings written to the file successfully.")

# Function to check if a number is prime
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

# Open the file in write mode
with open("prime_numbers.txt", "w") as file:
    # Write all prime numbers between 600 and 800 to the file
    for num in range(600, 801):
        if is_prime(num):
            file.write(str(num) + "\n")

print("Prime numbers written to the file successfully.")

import time

# Start the timer
start_time = time.time()

# Your program code here

# End the timer
end_time = time.time()

# Calculate the time taken
execution_time = end_time - start_time

print(f"Time taken: {execution_time} seconds")

# 12th question
import time
import matplotlib.pyplot as plt

def sort_list(num_elements):
    # Generate a list of random numbers
    lst = [random.randint(1, 100) for _ in range(num_elements)]
    
    # Start the timer
    start_time = time.time()
    
    # Sort the list
    lst.sort()
    
    # End the timer
    end_time = time.time()
    
    # Calculate the time taken
    execution_time = end_time - start_time
    
    return execution_time

# Number of elements in the list
num_elements = [5000, 10000, 15000, 20000, 25000]

# Time taken for sorting
time_taken = []

# Calculate the time taken for each number of elements
for num in num_elements:
    time_taken.append(sort_list(num))

# Plot the graph
plt.plot(num_elements, time_taken)
plt.xlabel("Number of Elements")
plt.ylabel("Time Taken (seconds)")
plt.title("Sorting Time vs Number of Elements")
plt.show()

# Q No. 13
def find_max_min_average_marks(student_marks):
    max_average = float('-inf')
    min_average = float('inf')
    max_student = None
    min_student = None
    
    for student, marks in student_marks.items():
        # Calculate the average marks
        average_marks = sum(marks) / len(marks)
        
        # Check for maximum average marks
        if average_marks > max_average:
            max_average = average_marks
            max_student = student
        
        # Check for minimum average marks
        if average_marks < min_average:
            min_average = average_marks
            min_student = student
    
    return max_student, min_student

# Dictionary of student marks
student_marks = {
    "John": [80, 85, 90, 75, 95],
    "Alice": [70, 75, 80, 85, 90],
    "Bob": [60, 65, 70, 75, 80],
    "Emily": [90, 95, 85, 80, 75],
    "David": [75, 80, 85, 90, 95]
}

# Find the student with maximum and minimum average marks
max_student, min_student = find_max_min_average_marks(student_marks)

# Print the results
print("Student with maximum average marks:", max_student)
print("Student with minimum average marks:", min_student)





