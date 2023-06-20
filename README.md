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

