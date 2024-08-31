# number-exploration

name=str(input("Enter your name "))
nums =[]
for i in range(0,3):
    num = int(input(f"Enter the {i} number "))
    nums.append(num)

print(f"Hello, {name}! Let's explore your favorite numbers:")  

even_odd_info = []
for num in nums:
    if num % 2 == 0:
        even_odd_info.append((num, "even"))
    else:
        even_odd_info.append((num, "odd"))

for info in even_odd_info:
    print(f"The number {info[0]} is {info[1]}.")

for num in nums:
    square_tuple = (num, num ** 2)
    print(f"The number {num} and its square: {square_tuple}")
    
sum=nums[0]+nums[1]+nums[2]       
print(f"Amazing! The sum of your favorite numbers is:{sum}")

def is_prime(n):
    if n <= 1:
        return False
    if n == 2:
        return True
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

if is_prime(sum):
    print(f"Wow, {sum} is a prime number!")
else:
    print(f"{sum} is not a prime number, but it’s still special!")
