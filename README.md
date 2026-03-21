# TCS-Practice-File

Ques-1. A parking lot charges vehicles based on the number of hours they are parked. The charges are as follows:
- For the first 2 hours, the rate is ₹100 per hour.
- For the next 3 hours (i.e., from hour 3 to hour 5), the rate is ₹50 per hour.
- Beyond 5 hours, the rate is ₹20 per hour.
-->Example 1:
  Input: 2
  Output: 200
  Example 2:
  Input: 4
  Output: 300
  Example 3:
  Input: 7
  Output: 360
  Input: 8
  Output: 410

Code: 

a=int(input())
a1=100
a2=50
a3=20
if a<=2:
    print(a*a1)
elif a>2 and a<=5:
    print(2*a1+(a-2)*a2)
else:
    print(2*a1+3*a2+(a-5)*a3)


Ques-2. A gym offers membership plans based on the number of months a person subscribes. The charges are fixed for certain durations:
- 1 month → ₹2000
- 3 months → ₹5000
- 6 months → ₹9000
- 9 months → ₹12000
- 12 months → ₹15000
Write a program that takes the number of months (a) as input and prints the membership fee.
If the input does not match any of the available plans, the program should print "Error".

---> Example 1:
Input: 1
Output: 2000
Example 2:
Input: 6
Output: 9000
Example 3:
Input: 5
Output: Error

Code:
### 1st Method ###

p=int(input())
plans={1:2000,3:5000,6:9000,9:12000,12:15000}
if p in plans:
    print(plans[p])
else:
    print("Error")

### 2nd Method ###
    
a=int(input())
if a==1:
    print("2000")
elif a==3:
    print("5000")
elif a==6:
    print("9000")
elif a==9:
    print("12000")
elif a==12:
    print("15000")
else:
    print("Error")

Ques-3: A gym offers membership plans with different pricing rules depending on the number of months a customer subscribes. The charges are structured as follows:
- For up to 2 months, the cost is ₹2000 per month.
- For exactly 3 months, the cost is ₹5000.
- For more than 3 months and less than 6 months, the cost is ₹5000 for the first 3 months plus ₹2000 per month for each additional month.
- For exactly 6 months, the cost is ₹9000.
- For more than 6 months and less than 9 months, the cost is ₹9000 for the first 6 months plus ₹2000 per month for each additional month.
- For exactly 9 months, the cost is ₹12000.
- For more than 9 months and less than 12 months, the cost is ₹12000 for the first 9 months plus ₹2000 per month for each additional month.
- For exactly 12 months, the cost is ₹15000.
- Any other input is considered Invalid.
Write a Python program that takes the number of months (a) as input and prints the total gym membership fee according to the above rules.

Examples:
Input: 2
Output: 4000
Input: 3
Output: 5000
Input: 5
Output: 9000
Input: 7
Output: 11000
Input: 12
Output: 15000
Input: 4
Output: 7000

code:

a=int(input())
if a <= 2:
    print(a*2000)
elif a == 3 :
    print(a*5000)
elif a > 3 and a < 6:
    print(1*5000+(a-3)*2000)
elif a == 6:
    print(a*9000)
elif a > 6 and a < 9:
    print(1*9000+(a-6)*2000)
elif a == 9:
    print(a*12000)
elif a > 9 and a < 12:
    print(1*12000+(a-9)*2000)
elif a == 12:
    print(a*15000)
else:
    print("Invalid Input")






