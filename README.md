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

Ques-4: A shop offers discounts on purchases based on the total bill amount. The discount rules are:
- If the purchase amount is greater than 0 and less than 1000, the customer gets a 5% discount.
- If the purchase amount is greater than 1000 and less than 5000, the customer gets a 10% discount.
- If the purchase amount is greater than 5000, the customer gets a 15% discount.
- For any other input (like negative values ), the program should print "Error".
Write a program that takes the purchase amount (p) as input and prints the final amount after discount.

Examples:
Input: 500
Output: 475.0
Input: 2000
Output: 1800.0
Input: 6000
Output: 5100.0
Input: -1000
Output: Error

code: 

p=int(input())
if p==0 and p<1000:
    print(p-p*5/100)
elif p>1000 and p<5000:
    print(p-p*10/100)
elif p>5000:
    print(p-p*15/100)
else:
    print("Error")


Ques-5: Problem Statement: Hot Air Balloon Ride Capacity
A group of tourists is waiting to board a hot air balloon. Each tourist has a certain weight. The balloon has a maximum weight capacity, and once this limit is reached, no more passengers can be added.
You are given:
- A list of integers representing the weights of the tourists in the order they arrive.
- An integer representing the maximum weight capacity of the balloon.
Write a program to determine how many tourists can board the balloon before the maximum capacity is exceeded.
Input Format:
- First line: space-separated integers representing the weights of tourists.
- Second line: an integer representing the maximum weight capacity of the balloon.
Output Format:
- Print the number of tourists who can successfully board the balloon.
Example Input 1:
40 50 60 30 20  
150
Output:
4 

Code:

a=list(map(int,input().split()))
Max_weight=int(input())
a.sort()
Total_weight=0
count=0
for p in a:
    if Total_weight+p <= Max_weight:
        Total_weight+=p
        count+=1
    else:
        break
print(count)


Ques-6: Favorite Movie Position After Sorting
You are given:
An array of movie IDs (all unique)
An integer K (1-based index)
Task:
Identify the movie at position K in the original array
Sort the array in ascending order
Find the new position (1-based index) of that movie after sorting
Example Input 1: 
4
1 3 2 4
2
Output:
2

Example Input 2: 
4
1 3 2 4
3
Output:
3

Code:

###### Method 1: { Using Dummy Element} ######

s=int(input())
p=[0]+list(map(int,input().split()))
p.sort()
print(p)
k=int(input())
print(p[k])

###### Method 2: {Using Index Method} ######

s=int(input())
p=list(map(int,input().split()))
p.sort()
print(p)
k=int(input())
fav=p[k]
print(p.index(fav))

###### Method 2: {Using Find Method} ######

s=int(input())
p=list(map(int,input().split()))
p.sort()
print(p)
k=int(input())
fav=p[k]
print(p.find(fav))


Ques-7: Given 
N=4:
Arr[20.25,30,35]
These are the prices of ticket in movie theater
We have to find all odd prices
and then output
Sum of odd prices, count of odd prices and average of odd prices
Example output:
60  2  30.00

question : ->>> A cinema hall sells tickets at different prices for different shows. The manager wants to analyze the ticket prices to find out:
- The sum of all ticket prices that are odd numbers.
- The count of how many odd-priced tickets exist.
- The average of these odd ticket prices.
Write a program that takes a list of ticket prices as input and calculates these three values.
Example input:
4
[20,25,30,35]

Example output:
60  2  30.00
where;
sum=60
count=2
avg=30.00

Code:

a=list(map(int,input().split()))
sum=0
count=0
avg=0
for i in a:
    if i%2!=0:
        sum+=i
        count+=1
        avg=sum/2
print(sum,count,f"{avg:.2f}")


Ques-8: Problem Statement: Sandwich Cost Closest to Budget
A café offers two lists of items:
- List A contains the prices of different types of bread.
- List B contains the prices of different fillings.
A customer wants to buy a sandwich by combining one bread and one filling. The café has set a budget limit (Target), and the customer wants the sandwich whose cost is closest to but less than the Target.
Write a program to:
- Read two lists of integers representing bread and filling prices.
- Read an integer Target representing the maximum budget.
- Find all possible sandwich costs (bread + filling) that are strictly less than Target.
- Print the sandwich cost that is closest to Target (i.e., the largest valid sum).
- Example input: 10 20 30
5 15
40
Example output:
Sandwich cost closest to Target is 35

Code: 

a=list(map(int,input().split()))
b=list(map(int,input().split()))
Target=int(input())
l=[]
for i in a:
    for j in b:
        if i+j<Target:
            l.append(i+j)
print("sandwitch cost Closet to Target is", l[-1])


























