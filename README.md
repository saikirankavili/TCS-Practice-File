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
            l.sort()
print("sandwitch cost Closet to Target is", l[-1])


Ques-9: Write a Python program that takes a string as input and checks whether it is a palindrome.
- Ignore case sensitivity (treat uppercase and lowercase letters as the same).
- Consider only alphanumeric characters (ignore spaces, punctuation, and special symbols).
- Print "yes" if the string is a palindrome, otherwise print "no".
Example input1: Racecar           
Output: yes
Example input2: hello
output: no
Example input3: a man a plan a canal panama
output: yes {ignoring spaces and case}

code:

p=input("Enter a string:")
s=""
for ch in p:
  if ch.isalnum():
   s+=ch.lower()
if s==s[::-1]:
  print("yes")
else:
  print("no")


Ques-10: Write a program to find sum of the digits in a given number
Example 1:
    Input: 1234
    Output: 10
Example 2:
    Input: 12345
    Output: 15

Code: 

### Method - 1 ###

p=int(input("enter a digit:"))
sum=0
for i in str(p):
    sum+=int(i)
print(sum)

### Method - 2 ###

p=input("enter a digit:")
sum=0
for i in p:
    sum+=int(i)
print(sum)


Ques-11: Write a Python program that:
- Accepts the user’s total income.
- Allows the user to enter multiple expenses (name and amount) until they type "done".
- Calculates and displays the total income, total expenses, and total savings.
- Prints an analysis showing each expense type with its corresponding amount.
Your code is the solution to this problem. For example:
- Input:
Enter income: 1000
Enter type of expense or 'done': Rent
Enter price of expense: 300
Enter type of expense or 'done': Food
Enter price of expense: 200
Enter type of expense or 'done': done
- Output:
Summary of Expenses:
Total Income: 1000.0
Total Expenses: 500.0
Total Savings: 500.0

Analysis:
Rent: 300.0
Food: 200.0

Code:

### Method-1 Beginner Level ###

p1=float(input("enter income:"))
p2=input("enter type of expense or done:")
p3=float(input("enter price if expense:"))
p4=input("enter type of expense or done:")
p5=float(input("enter price if expense:"))
print("Summary of Expenses:")
print(f'Total Income:{p1}')
print(f'Total Expenses:{p3+p5}')
print(f'Total Savings: {p1-(p3+p5)}')
print("Analysis:")
print(f'{p2}:{p3}')
print(f'{p4}:{p5}')

### Method-2 Advanced Level ###

income = float(input("Enter income: "))
expenses = {}  
while True:
    expense_type = input("Enter type of expense or 'done': ")
    if expense_type == "done" or expense_type == "Done":
        break
    price = float(input("Enter price of expense: "))
    expenses[expense_type] = price
    
print("\nSummary of Expenses:")
print(f"Total Income: {income}")
total_expenses = sum(expenses.values())
print(f"Total Expenses: {total_expenses}")
print(f"Total Savings: {income - total_expenses}")

print("\nAnalysis:")
for exp, amt in expenses.items():
    print(f"{exp}: {amt}")

Ques-12: Remove Duplicates and Print in Reverse
Problem Statement: You are given an array of integers. Your task is to remove all duplicate elements while preserving the order of their first occurrence, and then print the resulting array in reverse order.

Input Format
The first line contains an integer 𝑛, the length of the array.

The second line contains 𝑛, space‑separated integers representing the array elements.

Output Format
Print the modified array (with duplicates removed) in reverse order, with elements separated by spaces.

Example :
Input:
7
1 2 3 4 2 5 6
Output:
5 4 3 2 1

Code:::

Method : 1--->>> Time Complexity o(n^2)

p=int(input("Enter the Length of array:"))
s=list(map(int,input().split()))
k=[]
for i in s:
  if i not in k:
    k.append(i)
print(*k[::-1])

Method : 2--->>> Time Complexity o(n)

p=int(input("Enter the Length of array:"))
s=list(map(int,input().split()))
k=[]
seen = set()
for i in s:
  if i not in seen:
    seen.add(i)
    k.append(i)
print(*k[::-1])
  
Ques-13: Calculate Speed
Problem Statement: You are tasked with writing a program that calculates the speed of an object given the distance traveled and the time taken. The time will be provided in minutes, and you must convert it into hours before computing the speed. If the input time is not within the valid range (1 to 60 minutes), the program should output an error message.

Input Format:
The first line contains an integer 𝑑, representing the distance traveled (in kilometers).

The second line contains an integer 𝑡, representing the time taken (in minutes).

Output Format:
Print the calculated speed (in kilometers per hour).

If the time is invalid, print "error".

Example:
Input:
Distance:30km
Speed:30min
Output:
60
Explanation:
Time in hrs: 30/60=0.5
Speed: 30/0.5=60kmph

code:::

Approach-1:--->

p=int(input("Enter the distance:"))
s=int(input("Enter the time:"))
if s>=1 and s<=60:
    print(int(p*60)/s)
else:
    print("error")

Approach-2:--->

p=int(input("Enter the distance:"))
s=int(input("Enter the time:"))
if s>=1 and s<=60:
  k=s/60 
  print(p/k)
else:
    print("error")

Ques-14: Eligible Laptops for Meeting
Problem Statement: A company is organizing an online meeting and wants to ensure that only laptops with sufficient specifications are eligible to join. Each laptop has a performance score, and the company sets a minimum required score 
𝑘.Your task is to determine how many laptops meet or exceed this requirement.

Input Format
The first line contains an integer 𝑛, representing the number of laptops.

The second line contains 𝑛, space‑separated integers, each representing the performance score of a laptop.

The third line contains an integer 𝑘, the minimum required score for eligibility.

Output Format
Print the number of laptops whose performance score is greater than or equal to 𝑘.

  Example:
  Input:
  5
  20 30 50 60 70
  50
  Output:
  3

  Code:::

s=int(input("Enter the range: "))
p=list(map(int,input().split()))
k=int(input())
count=0
for i in p:
    if i>=k:
        count+=1
print(count)

























