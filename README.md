#This program calculates the electric bill based on the number of units consumed
#The rates are as follows:
#The program is made as user friendly by providing clear instructions and prompts
print("Welcome to the Electric Bill Calculator!")
print("\ncustomer bill details :")
print("    units     -    rupees/unit    ")
print("    50-100    -       3 ")
print("    100-150   -       5 ")
print("    150-200   -       7 ")  
print("\nFor above 200 units : 10 rupees/unit")
print("Minimum charges : 150 rupees\n") 

#Calculating electric bill based on units consumed
#Using input function to take user input for number of units consumed
#Using conditional statements and if-elif-else and arithmetic operations to calculate the bill

unit = int(input("Enter the number of units consumed: "))
if unit>=50 and unit<=100:
    bill = unit * 3
    print(f"Your electric bill is: {bill} rupees")
elif unit>=100 and unit<=150: 
    bill = unit * 5
    print(f"Your electric bill is: {bill} rupees")
elif unit>=150 and unit<=200:
    bill = unit * 7
    print(f"Your electric bill is: {bill} rupees")   
elif unit>200:
    bill = unit * 10
    print(f"Your electric bill is: {bill} rupees")
else:
    bill = 150
    print(f"min charges applied: {bill} rupees")

#Calculating expected bill based on last 6 months consumption
print("\nEnter bill of each month separated by space.For example: 1 2 20 25 30 35")
s = input("Enter bill of 6 months : ")
months = [int(x) for x in s.split()]   
expected_bill = 0
avg = 0
#Calculating average bill of last 6 months using for loop
for i in range (len(months)):
    avg += months[i]
    i = +1 
    expected_bill = avg / len(months)
print(expected_bill)       
