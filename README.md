# MathStuff
#Mean, Median, Mode 

#For Slight Convenience
import time as t

#This is to help count duplicate things in a list
from collections import Counter

#Mean Function (Finds average in list)
def mean():
    n_num = [9, 14, 17, 12, 11]
    n = len(n_num)
 
    get_sum = sum(n_num)
    mean = get_sum / n
 
    print("Mean is: " + str(mean))

#Median Function (Finds middle number essentially)
def median():
    n_num = [8, 15, 12, 17, 11, 18, 23, 16]
    n = len(n_num)
    n_num.sort()
 
    if n % 2 == 0:
        median1 = n_num[n//2]
        median2 = n_num[n//2 - 1]
        median = (median1 + median2)/2
    else:
        median = n_num[n//2]
    print("Median is: " + str(median))

#Mode Function (Finds number that has the most duplicates)
def mode():
    n_num = [3, 3, 3, 9, 2, 6]
    n = len(n_num)
 
    data = Counter(n_num)
    get_mode = dict(data)
    mode = [k for k, v in get_mode.items() if v == max(list(data.values()))]
 
    if len(mode) == n:
        get_mode = "No mode found"
    else:
        get_mode = "Mode is / are: " + ', '.join(map(str, mode))
    print(get_mode)

#The answer to all your questions (Real, Not Fake)
mean()
t.sleep(1)
median()
t.sleep(1)
mode()
