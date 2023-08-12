
## Question 1

Write a program to output Hello, World! on the console


Solution:
```python
print("Hello, World!")
```

## Question 2

Write a program to display the sum of first n numbers


Solution:
```python
n = int(input("Enter a positive integer n: "))
if n <= 0:
    print("Please enter a positive integer.")
else:
    sum = 0
    for i in range(1, n + 1):
        sum += i
    print(f"The sum of the first {n} natural numbers is: {sum}")
```

## Question 3

Write a program to calculate the factorial of first n numbers


Solution:
```python
n = int(input("Enter a number: "))
factorial = 1
if num < 0:
   print("Sorry, factorial does not exist for negative numbers")
elif num == 0:
   print("The factorial of 0 is 1")
else:
   for i in range(1,n + 1):
       factorial = factorial*i
   print("The factorial of",n,"is",factorial)
   ```



## Question 4

Write a program to calculate the sum of two numbers input together with a whitespace

Input : 2 3\
Output : 5


Solution:
```python
i=int(input())
while True:
    a,b=input().split()
    c=int(a)+int(b)
    print(c)
    i-=1
    if i==0:
        break
```

## Question 5   

### CCC '14 J1 - Triangle Times
Canadian Computing Competition: 2014 \
You have trouble remembering which type of triangle is which. You write a program to help. Your program reads in three angles (in degrees).\
If all three angles are , output **Equilateral** .\
If the three angles add up to and exactly two of the angles are the same, output **Isosceles** .\
If the three angles add up to and no two angles are the same, output **Scalene** .\
If the three angles do not add up to , output **Error**


Solution:
```python
while True:
    a1=int(input())
    if a1<0 or a1>180:
        break
    a2=int(input())
    if a2<0 or a2>180:
        break
    a3=int(input())
    if a3<0 or a3>180:
        break
    if a1+a2+a3==180:
        if a1==a2==a3==60:
            print("Equilateral")
            break
        if a1!=a2 and a2!=a3 and a1!=a3:
            print("Scalene")
            break
        if a1==a2 or a2==a3 or a3==a1:
            print("Isosceles")
            break
    else:
        print("Error")
        break
```


## Question 6

Write a program which will find all such numbers which are divisible by 7 but are not a multiple of 5, between 2000 and 3200 (both inclusive). The numbers obtained should be printed in csv on a single line.


Solution:
```python
l=[]
for i in range(2000, 3201):
    if (i%7==0) and (i%5!=0):
        l.append(str(i))

print(','.join(l))
```


## Question 7

Write a program which accepts a sequence of comma-separated numbers from console and generate a list and a tuple which contains every number

Solution:
```python
values=input()
l=values.split(",")
t=tuple(l)
print(l)
print(t)
```
## Question 8

### CCC '12 J1 - Speed fines are not fine!
Canadian Computing Competition: 2012 Stage 1, Junior #1
Many communities now have "radar" signs that tell drivers what their speed is, in the hope that they will slow down.
You will output a message for a "radar" sign. The message will display information to a driver based on his/her speed
according to the following table:

>
 km/h over the limit|  Fine |
 ----------- | ----------- |
 1 to 20  | $100 |
 21 to 30  |$270  |
 31 or above |$500 |
 
The user will be prompted to enter two integers. First, the user will be prompted to enter the speed limit. Second, the
user will be prompted to enter the recorded speed of the car.

If the driver is not speeding, the output should be: **Congratulations, you are within the speed limit!**\
If the driver is speeding, the output should be: **You are speeding and your fine is $F**. where F is the amount
of the fine as described in the table above.



Solution:
```python
limit=float(input())
act_speed=float(input())
if act_speed<=limit:
    print("Congratulations, you are within the speed limit!")
diff=act_speed-limit
if act_speed>limit:
    if diff<=20 and diff>=1:
        fine=100
    if diff<=30 and diff>=21:
        fine=270
    if diff>=31:
        fine=500
    print("You are speeding and your fine is $"+str(fine)+".")
```
## Question 9

Write a program to count the vowels in a string and replace them with an asterisk (*)  

hint :  Strings are immutable 

Solution:
```python
a=input()
count=0
for i in a:
    if i=='a' or i=='e' or i=='i' or i=='o' or i=='u':
        count+=1


print(count)
print(a.replace('a','*').replace('e','*').replace('i','*').replace('o','*').replace('u','*'))
```
## Question 10

Write a program for sum/product of values in a tuple.

Solution:
```python
t=(1,2,3,4,5)
sum=0
prod=1
for i in t:
    sum+=i
    prod*=i
print(sum)
print(prod)

```
## Question 11

A website requires the users to input username and password to register. Write a program to check the validity of password input by users. Following are the criteria for checking the password:\
1. At least 1 lowercase letter 
2. At least 1 number 
3. At least 1 uppercase letter
4. At least 1 special character 
5. Minimum length of transaction password: 6
6. Maximum length of transaction password: 12


Solution:
```python
a=input()
upper_case=0
lower_case=0
special_char=0
digits=0

for i in a:
    if i.isupper():
        upper_case+=1
    if i.islower():
        lower_case+=1
    if i.isdigit():
        digits+=1
    if not i.isalnum():
        special_char+=1

if len(a)>=6 and len(a)<=12 and upper_case>=1 and lower_case>=1 and digits>=1 and special_char>=1:
    print('Valid')
else:
    print('Invalid')
```
## Question 12

Write a program to take in name, age and gender of a person and add them in a nested list (eg-[ [name,age,gender], [name,age,gender] ])

hint : use of copy() as later we empty the same list

Solution:
```python
l=[]
l1=[]
n=int(input('Enter number of people to be added: '))
for i in range(n):
    for j in range(3):
        a=input()
        l1.append(a)
    l.append(l1.copy())
    l1.clear()
print(l)

```
## Question 13

Convert a number to string using functions.


Solution:
```python
def conv(n):
    n=str(n)
    print(n,type(n))

n=int(input())
conv(n)
```
## Question 14

Define a function that can accept an integer number as input and print the **It is an even number** if the number is even, otherwise print **It is an odd number**.

Solution:
```python
def odd_eve(n):
    if n%2==0:
        print('It is an even number')
    else:
        print('It is an odd number')
n=int(input())
odd_eve(n)

```
## Question 15

Write a program to find the hypotenuse of a rt. angled triangle.

Solution:
```python
s1=int(input('Enter known side: '))
s2=int(input('Enter known side: '))
h=(s1**2)+(s2**2)
h=h**0.5
print(h)
```
## Question 16

Define a function which can generate and print a list where the values are square of numbers between 1 and 20 (both included).

Solution:
```python
def printList():
	li=list()
	for i in range(1,21):
		li.append(i**2)
	print(li)

printList()
```
## Question 17

Write a function to compute 5/0 and use try/except to catch the exceptions.


Solution:
```python
def throws():
    return 5/0

try:
    throws()
except ZeroDivisionError:
    print("division by zero!")
except Exception, err:
    print('Caught an exception')
finally:
    print('In finally block for cleanup')
```
## Question 18

Please write a program using generator to print the numbers which can be divisible by 5 and 7 between 0 and n in comma separated form while n is input by console.


Solution:
```python
def NumGenerator(n):
    for i in range(n+1):
        if i%5==0 and i%7==0:
            yield i

n=int(input())
values = []
for i in NumGenerator(n):
    values.append(str(i))

print(",".join(values))
```
## Question 19

With two given lists [1,3,6,78,35,55] and [12,24,35,24,88,120,155], write a program to make a list whose elements are intersection of the above given lists.

hint : Use set() and "&=" to do set intersection operation.

Solution:
```python
set1=set([1,3,6,78,35,55])
set2=set([12,24,35,24,88,120,155])
set1 &= set2
li=list(set1)
print(li)
```
## Question 20

Write a program to output the full form of abrevations VIT, BRB, TTYL and print  **/-** if another abrevation is entered


Solution:
```python
Abrevations={
    "VIT":"Vellore Institute of Technology",
    "BRB":"Be right back",
    "TTYL":"Talk to you later",
}
words=input("Enter the abrevation (in all caps) ")
if words=="VIT":
    print(Abrevations.get("VIT"))
if words=="BRB":
    print(Abrevations.get("BRB"))
if words=="TTYL":
    print(Abrevations.get("TTYL"))
else:
    print("/-")
```
## Question 21

Write a program to output an asterisk triangle of base n


Solution:
```python
i=int(input("Enter the length of base of triange - "))
while True:
    print("*"*i)
    i=i-1
    if i==0:
        break
```
## Question 22

Write a program to be used as a bill calculated that takes in parameters of cost and quantity and calculates the total amount, use f-strings for displaying the output


Solution:
```python
total_bill = 0
num_items = int(input("Enter the number of items: "))
for item in range(1, num_items + 1):
    print(f"Item {item}:")
    cost = float(input("Enter the cost of the item: "))
    quantity = int(input("Enter the quantity of the item: "))
    item_total = cost * quantity
    print(f"Total amount for item {item}: {item_total:.2f}")
    total_bill += item_total

print(f"Total bill amount: {total_bill:.2f}")
```
## Question 23

Write a program to print out a n sided regular polygon from input by user using the turtle library


Solution:
```python
import turtle
ttle=turtle.Pen()
ttle.pencolor("black")
sides=int(input("How many sides does the polygon "))
angle_rotxn=360/sides
while 0<2:
    ttle.forward(90)
    ttle.left(angle_rotxn)
```
## Question 24

Write a program to print a random spiral pattern using turtle library 


Sample solution:
```python
import random
import turtle
ttle=turtle.Pen()
colors=["blue","red","green","yellow","orange","white"]
turtle.bgcolor("black")
ttle.speed(33)
while 0<2:
    ttle.circle(random.randint(21,87))
    ttle.pencolor(random.choice(colors))
    ttle.left(random.randint(31,79))
    ttle.pencolor(random.choice(colors))
    ttle.forward(random.randint(21,87))
    ttle.pencolor(random.choice(colors))
```
## Question 25

Write a program to output random characters on the screen in a matrix like pattern


Solution:
```python
import random
import time

numlist=['1','2','3','4','5','6','7','8','9','0']
alphabetlist=['q','w','e','r','t','y','u','i','o','p','a','s','d','f','g','h','j','k','l','z','x','c','v','b','n','m']
cap_alpbahetlist=['Q','W','E','R','T','Y','U','I','O','P','A','S','D','F','G','H','J','K','L','Z','X','C','V','B','N','M']
symb = ['@', '#', '$', '%', '=', ':', '?', '.', '/', '|', '~', '>','*', '(', ')', '<']

while True:
    rand_chars=random.choices(numlist,k=1000)
    rand_chars_a=random.choices(alphabetlist,k=1000)
    rand_chars_b=random.choices(cap_alpbahetlist,k=1000)
    rand_chars_c=random.choices(symb,k=1000)
    rand=rand_chars_a+rand_chars+rand_chars_b+rand_chars_c
    i=random.randint(2,12)  
    time.sleep(0.01)
    print((" "*i).join(random.choices(rand,k=30)))
```
## Question 26

Write a program to encrypt/decrypt numbers


Sample solution:
```python
while True:
    wt_todo=input("Encrypt(e) or Decrypt(d) ? ")
    if wt_todo=="e":
        numbr=int(input("Enter number "))
        nw_numbr=(numbr*4)-21
        print("The encrypted number is ",nw_numbr)
    if wt_todo=="d":
        nmbr=int(input("Enter number "))
        nw_nmbr=(nmbr+21)/4
        print("The decrypted number is ",nw_nmbr)
```
## Question 27

Write a program to calculate the determinant of a 3x3 matrix


Solution:
```python
print("In the format - ")
print("[a  b  c] ")
print("[d  e  f] ")
print("[g  h  i] ")
a=int(input("a = ? "))
b=int(input("b = ? "))
c=int(input("c = ? "))
d=int(input("d = ? "))
e=int(input("e = ? "))
f=int(input("f = ? "))
g=int(input("g = ? "))
h=int(input("h = ? "))
i=int(input("i = ? "))
print("")
print("")
print("[ ",a  ,b,  c," ] ")
print("[ ",d  ,e , f," ] ")
print("[ ",g , h , i," ] ")
print((a*e*i)-(a*f*h)-(b*d*i)+(b*g*f)+(c*d*h)-(c*g*e))
```
## Question 28

Write a program to output the arguement and euler's form of a complex number


Solution:
```python
import math
print("Z= a + ib ")
a=int(input("Enter a - "))
b=int(input("Enter b - "))
c=b/a
angle=math.degrees(math.atan(c))
print("The arguement is ",angle)
r=math.sqrt((a**2)+(b**2))
print("Eulers form is - ",r , "e^i",angle)
```
## Question 29

Write a program to replace the alphabetss of string by the next alphabet


Solution:
```python
a=input("Enter the word ")
length=len(a)
i=0
new_word_list=[]
while i<length:
    asc=ord(str(a[i]))
    asc+=1
    new_word_list.append(chr(asc))
    i+=1
z="".join(new_word_list)
print(z)
```
## Question 30

Write a program to output all the factors of a number

Solution:
```python
n=int(input("Enter number - "))
i=2
print("1 is a factor ")
while 0<2:
    z=(n/i)-(n//i)
    if z==0:
        print(i, "Is a factor")
    if i==n:
        break
    i=i+1
```

## Question 31

Write a program to guess what number the user is thinking of from 0-5


Sample solution:
```python
print("I can guess what number ur thinking of bw 0-5")
print("Lets start")
oen=input("Is ur no. even(e) or odd(o) or neither(n) ")
if oen =="n":
    print("your no. is **  ZERO  ** ")
if oen =="e":
    e_psq=input("Is the number a perfect square? y/n ")
    if e_psq=="y":
        print("your number is **  FOUR  **")
    if e_psq=="n":
        print("your number is ** TWO  **")
if oen=="o":
    o_psq=input("Is your number a perfect square ? y/n ")
    if o_psq=="y":
        print("your number is **  ONE  **")
    if o_psq=="n":
        fibo=input("Is your number part of the fibonacci series ? y/n ")
        if fibo=="y":
            print("your number is **  THREE  **")
        if fibo=="n":
            print("your number is ** FIVE  **")
```

## Question 32

Write a program to generate random strong passwords


Sample solution:
```python
import random
print("\n\n\n\nWelcome to password generation portal !!\n")
print("Press return to continue\n")
input()

numlist=['1','2','3','4','5','6','7','8','9','0']
alphabetlist=['q','w','e','r','t','y','u','i','o','p','a','s','d','f','g','h','j','k','l','z','x','c','v','b','n','m']
cap_alpbahetlist=['Q','W','E','R','T','Y','U','I','O','P','A','S','D','F','G','H','J','K','L','Z','X','C','V','B','N','M']
symb = ['@', '#', '$', '%', '=', ':', '?', '.', '/', '|', '~', '>','*', '(', ')', '<']

nm=random.choices(numlist,k=2)
al=random.choices(alphabetlist,k=6)
c_al=random.choices(cap_alpbahetlist,k=3)
sl=random.choices(symb,k=3)

passwd=nm+al+c_al+sl
f_passwd="".join(passwd)
print("New password for you - ",f_passwd)
```

## Question 33

Write a program to manage passwords on python in an external file


Solution:
```python
from asyncore import read
import sys
ids=open("passwords.txt","r+")
content=ids.read()
master_pass=input("Enter Master Password -> ")
if master_pass=="0208":
    read_write=input("List old passwords(1) or Add new ones(2) ")
    while True:
        if read_write=="1":
            print(content)
            break
        if read_write=="2":
            website=input("Website Name -> ")
            new_usrname=input("Enter New Username -> ")
            new_pass=input("Enter New Password -> ")
            ids.write("\n"+website+"_username = "+new_usrname)
            ids.write("\n"+website+"_password = "+new_pass)
            break
if master_pass!="0208":
    print("Thats not the passowrd FOOL! ")
    sys.exit()
ids.close() 
```

## Question 34

Write a program to output the total time since birth for an entered name


Solution:
```python
namee=input("Enter your name ")
age=input("Enter your age ")
print("Good Day ",namee)
print("You have been alive for ",int(age)*365*24*60*60, " seconds")
print("You have been alive for ",int(age)*365*24*60, " minutes")
print("You have been alive for ",int(age)*365*24, " hours")
print("You have been alive for ",int(age)*365, " days")
print("Good job",namee,"!")
```

## Question 35

Write a program to simulate a bank in python using external files, asume it to run for eternity and no data loss


Solution:
```python
import random
i=1
print("*** WELCOME TO BANK OF INDIA ***")
print("What Can I help You With ")
while True:
    wt_todo=input("(1)Open a new account\n(2)Use existing account\n")
    if wt_todo=="1":
        new_acc=open("PY/BANK/bank_data","a")
        acc_num=i
        usr_name=input("Enter Name - ")
        usr_num=input("Enter Mobile Number - ")
        usr_ID=input("Enter Unique ID - ")
        usr_bal=input("Enter Amount to deposit - ")
        new_acc.write("\n Account number - "+str(i) )
        new_acc.write("     User Name - "+usr_name)
        new_acc.write("     User Mobile Number - "+usr_num)
        new_acc.write("     User Unique ID - "+usr_ID)
        new_acc.write("     User Balance - "+usr_bal)
        print("\n\n\n*** SUCCESS ***")
        print("User Account Number is - ",i)
        print("User Name is - ",usr_name)
        print("User Mobile Number is - ",usr_num)
        print("User Unique ID is - ",usr_ID)
        print("")
        print("________________________")
        print("Balance = ",usr_bal)
        print("________________________")
        input()
        new_acc.close()
        i=i+1
    if wt_todo=="2":
        acc_det=open("PY/BANK/bank_data","r")
        acc_num=input("Enter Account Number - ")
        lines=acc_det.readlines()
        print("\n\n",lines[int(acc_num)])
```

## Question 36

Write a Tic-Tac-Toe game in python


Solution:
<details>
    <summary>
        Code
    </summary>

```python
a="a";b="b";c="c";d="d";e="e";f="f";g="g";h="h";i="i"

#p1's turn 
print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
while True:
    #P1's TURN----------------------
    t_1=input("\nP1's turn -  ")
    if t_1=="a":
        a="X"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_1=="b":
        b="X"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_1=="c":
        c="X"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_1=="d":
        d="X"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_1=="e":
        e="X"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_1=="f":
        f="X"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_1=="g":
        g="X"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_1=="h":
        h="X"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_1=="i":
        i="X"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    
#P1 Winning condition

    if a=="X" and b=="X" and c=="X":
        print("P1 won!")
        break
    if a=="X" and e=="X" and i=="X":
        print("P1 won!")
        break
    if a=="X" and d=="X" and g=="X":
        print("P1 won!")
        break
    if c=="X" and f=="X" and i=="X":
        print("P1 won!")
        break
    if g=="X" and h=="X" and i=="X":
        print("P1 won!")
        break
    if d=="X" and e=="X" and f=="X":
        print("P1 won!")
        break
    if c=="X" and e=="X" and g=="X":
        print("P1 won!")
        break
    if b=="X" and e=="X" and h=="X":
        print("P1 won!")
        break

#P2's turn-----------------------

    t_2=input("\nP2's turn - ")
    if t_2=="a":
        a="O"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_2=="b":
        b="O"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_2=="c":
        c="O"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_2=="d":
        d="O"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_2=="e":
        e="O"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_2=="f":
        f="O"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_2=="g":
        g="O"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_2=="h":
        h="O"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    if t_2=="i":
        i="O"
        print("\n",a, b, c,"\n",d, e, f,"\n",g, h, i)
    
#P2's WINNING TERMS------------------------    

    if a=="O" and b=="O" and c=="O":
        print("P2 won!")
        break
    if a=="O" and e=="O" and i=="O":
        print("P2 won!")
        break
    if a=="O" and d=="O" and g=="O":
        print("P2 won!")
        break
    if c=="O" and f=="O" and i=="O":
        print("P2 won!")
        break
    if g=="O" and h=="O" and i=="O":
        print("P2 won!")
        break
        break
    if d=="O" and e=="O" and f=="O":
        print("P2 won!")
        break
    if c=="O" and e=="O" and g=="O":
        print("P2 won!")
        break
    if b=="O" and e=="O" and h=="O":
        print("P2 won!")
        break
```

</details>

## Question 37

Write a 2P Snake and Ladders game in python


Solution:
<details>
    <summary> 
Code
    </summary>

```python
import random
locxn_1p=0
locxn_2p=0
#P1's turn
 
while True:
    dice_P1=random.randint(1,6)
    if dice_P1==6:
        print("P1 threw the dice - ",dice_P1,"\nP1 gets another turn ")
        locxn_1p=int(locxn_1p)+int(dice_P1)
        if locxn_1p==locxn_2p:
            locxn_2p=0
            print("P1 cut P2")
        print("P1 landed at - ",locxn_1p," initially ")
        dice_P1_2=random.randint(1,6)
        print("P1 threw the dice again- ",dice_P1_2)
        locxn_1p=int(locxn_1p)+int(dice_P1_2)
        if locxn_1p==locxn_2p:
            locxn_2p=0
            print("P1 cut P2")
        print("P1 finally landed at - ",locxn_1p)
        input()
    else:
        print("P1 threw the dice - ",dice_P1)
        locxn_1p=int(locxn_1p)+int(dice_P1)
        if locxn_1p==locxn_2p:
            locxn_2p=0
            print("P1 cut P2")
        print("P1 landed at - ",locxn_1p)
        input()
#P2's turn
    dice_P2=random.randint(1,6)
    if dice_P2==6:
        print("P2 threw the dice - ",dice_P2,"\nP2 gets another turn ")
        locxn_2p=int(locxn_2p)+int(dice_P2)
        print("P2 landed at - ",locxn_2p," initially ")
        if locxn_1p==locxn_2p:
            locxn_1p=0
            print("P2 cut P1")
        dice_P1_2=random.randint(1,6)
        print("P2 threw the dice again - ",dice_P1_2)
        locxn_2p=int(locxn_2p)+int(dice_P1_2)
        if locxn_1p==locxn_2p:
            locxn_1p=0
            print("P2 cut P1")
        print("P2 finally landed at - ",locxn_2p)
        input()
    else:
        print("P2 threw the dice - ",dice_P2)
        locxn_2p=int(locxn_2p)+int(dice_P2)
        if locxn_1p==locxn_2p:
            locxn_1p=0
            print("P2 cut P1")
        print("P2 landed at - ",locxn_2p)
        input()

#------------------FOR P1---------------------
#Snakes
    if locxn_1p==21:
        print("SIKE! You got bit.")
        locxn_1p=int(15)
        print("You landed on",locxn_1p)
    if locxn_1p==23:   
        print("SIKE! You got bit.")
        locxn_1p=int(6)
        print("You landed on",locxn_1p)
    if locxn_1p==29:
        print("SIKE! You got bit.") 
        locxn_1p=int(15)
        print("You landed on",locxn_1p)
    if locxn_1p==35:
        print("SIKE! You got bit.")
        locxn_1p=int(18)
        print("You landed on",locxn_1p)
    if locxn_1p==32:
        print("SIKE! You got bit.")
        locxn_1p=int(47)
        print("You landed on",locxn_1p)
    if locxn_1p==52:
        print("SIKE! You got bit.") 
        locxn_1p=int(38)
        print("You landed on",locxn_1p)
    if locxn_1p==71:
        print("SIKE! You got bit.")
        locxn_1p=int(34)
        print("You landed on",locxn_1p)
    if locxn_1p==69:
        print("SIKE! You got bit.")
        locxn_1p=int(42)
        print("You landed on",locxn_1p)
    if locxn_1p==82:
        print("SIKE! You got bit.") 
        locxn_1p=int(59)
        print("You landed on",locxn_1p)
    if locxn_1p==95:
        print("SIKE! You got bit.")
        locxn_1p=int(32)
        print("You landed on",locxn_1p)
    if locxn_1p==99:
        print("SIKE! You got bit.")
        locxn_1p=int(79)
        print("You landed on",locxn_1p)
#Ladders
    if locxn_1p==2:
        print("YAY! You climbed up .") 
        locxn_1p=int(18)
        print("You landed on",locxn_1p)
    if locxn_1p==12:
        print("YAY! You climbed up .") 
        locxn_1p=int(28)
        print("You landed on",locxn_1p)
    if locxn_1p==11:
        print("YAY! You climbed up .") 
        locxn_1p=int(31)
        print("You landed on",locxn_1p)
    if locxn_1p==70:
        print("YAY! You climbed up .") 
        locxn_1p=int(94)
        print("You landed on",locxn_1p)
    if locxn_1p==85:
        print("YAY! You climbed up .") 
        locxn_1p=int(97)
        print("You landed on",locxn_1p)
    if locxn_1p==22:
        print("YAY! You climbed up .") 
        locxn_1p=int(40)
        print("You landed on",locxn_1p)
    if locxn_1p==41:
        print("YAY! You climbed up .") 
        locxn_1p=int(59)
        print("You landed on",locxn_1p)
    if locxn_1p==77:
        print("YAY! You climbed up .") 
        locxn_1p=int(84)
        print("You landed on",locxn_1p)
    if locxn_1p==46:
        print("YAY! You climbed up .") 
        locxn_1p=int(55)
        print("You landed on",locxn_1p)
    if locxn_1p==36:
        print("YAY! You climbed up .") 
        locxn_1p=int(62)
        print("You landed on",locxn_1p)
    if locxn_1p==41:
        print("YAY! You climbed up .") 
        locxn_1p=int(59)
        print("You landed on",locxn_1p)



#Snakes
    if locxn_2p==21:
        print("SIKE! You got bit.")
        locxn_2p=int(15)
        print("You landed on",locxn_2p)
    if locxn_2p==23:   
        print("SIKE! You got bit.")
        locxn_2p=int(6)
        print("You landed on",locxn_2p)
    if locxn_2p==29:
        print("SIKE! You got bit.") 
        locxn_2p=int(15)
        print("You landed on",locxn_2p)
    if locxn_2p==35:
        print("SIKE! You got bit.")
        locxn_2p=int(18)
        print("You landed on",locxn_2p)
    if locxn_2p==32:
        print("SIKE! You got bit.")
        locxn_2p=int(47)
        print("You landed on",locxn_2p)
    if locxn_2p==52:
        print("SIKE! You got bit.") 
        locxn_2p=int(38)
        print("You landed on",locxn_2p)
    if locxn_2p==71:
        print("SIKE! You got bit.")
        locxn_2p=int(34)
        print("You landed on",locxn_2p)
    if locxn_2p==69:
        print("SIKE! You got bit.")
        locxn_2p=int(42)
        print("You landed on",locxn_2p)
    if locxn_2p==82:
        print("SIKE! You got bit.") 
        locxn_2p=int(59)
        print("You landed on",locxn_2p)
    if locxn_2p==95:
        print("SIKE! You got bit.")
        locxn_2p=int(32)
        print("You landed on",locxn_2p)
    if locxn_2p==99:
        print("SIKE! You got bit.")
        locxn_2p=int(79)
        print("You landed on",locxn_2p)
#Ladders
    if locxn_2p==2:
        print("YAY! You climbed up .") 
        locxn_2p=int(18)
        print("You landed on",locxn_2p)
    if locxn_2p==12:
        print("YAY! You climbed up .") 
        locxn_2p=int(28)
        print("You landed on",locxn_2p)
    if locxn_2p==11:
        print("YAY! You climbed up .") 
        locxn_2p=int(31)
        print("You landed on",locxn_2p)
    if locxn_2p==70:
        print("YAY! You climbed up .") 
        locxn_2p=int(94)
        print("You landed on",locxn_2p)
    if locxn_2p==85:
        print("YAY! You climbed up .") 
        locxn_2p=int(97)
        print("You landed on",locxn_2p)
    if locxn_2p==22:
        print("YAY! You climbed up .") 
        locxn_2p=int(40)
        print("You landed on",locxn_2p)
    if locxn_2p==41:
        print("YAY! You climbed up .") 
        locxn_2p=int(59)
        print("You landed on",locxn_2p)
    if locxn_2p==77:
        print("YAY! You climbed up .") 
        locxn_2p=int(84)
        print("You landed on",locxn_2p)
    if locxn_2p==46:
        print("YAY! You climbed up .") 
        locxn_2p=int(55)
        print("You landed on",locxn_2p)
    if locxn_2p==36:
        print("YAY! You climbed up .") 
        locxn_2p=int(62)
        print("You landed on",locxn_2p)
    if locxn_2p==41:
        print("YAY! You climbed up .") 
        locxn_2p=int(59)
        print("You landed on",locxn_2p)


#Winning condition
    if locxn_1p>=100:
        print("YAY P1 Won ")
        break
    if locxn_2p>=100:
        print("YAY P2 Won ")
        break
```
</details>

## Question 38

### CCC '04 J2 - Terms of Office
Canadian Computing Competition: 2004\
In CS City, a mathematical place to live, the mayor is elected every 4 years, the treasurer is appointed every 2 years, the
chief programmer is elected every 3 years and the dog-catcher is replaced every 5 years.\
This year, Year X, the newly elected mayor announced the appointment of the new treasurer, a new dog-catcher and
congratulated the chief programmer for winning the recent election. That is, all positions were changed over. This is
highly unusual. You will quantify how unusual this really is.\
Write a program that inputs the year X and the future year Y and lists all years between X and Y inclusive when all
positions change.



Solution:
```python
x=int(input())
y=int(input())
while True:
    if x>y:
        break
    print("All positions change in year",x)
    x+=60
```

## Question 39

### Waterloo 2017 Winter A - Vera and Outfits
2017 Winter Waterloo Local ACM Contest\
Vera owns N tops and N pants. The i-th top and i-th pants have colour i, for 1<=i<=N , where all N colours are
different from each other.\
An outfit consists of one top and one pants. Vera likes outfits where the top and pants are not the same colour.
How many different outfits does she like?\

***Constraints:***\
1<=N<=2017\
N is integer

***Input Specification:*** \
The input will be in the format: N\

***Output Specification***\
Output one line with the number of different outfits Vera likes.

Solution:
```python
n=int(input())
outfits=(n*n)-n
print(outfits)
```

## Question 40

 Pomodoro Clock


## Question 41

CLI-ToDo List

## Question 42

Snake

## Question 43

Emoji Translator

## Question 44

Random username Generator


## Question 45

GUI-Bin2Dec

## Question 46

Make your own python library

## Question 47

CLI-Image extension changer using pillow

## Question 48

Mario like runner

## Question 49

Flappy Bird clone

## Question 50

Make a python tutorial


## ~suvansh gupta 
###  reach out to me at 

[@13suvansh](https://www.instagram.com/13suvansh/)