# lab activity 
# Task 1: The Basic Calculator

# 1. Assign two different numbers to variables a and b
a = 10
b = 3

# 2. Calculate and print the results
print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Floating-Point Division:", a / b)
print("Integer Division:", a // b)
print("Modulus:", a % b)
print("Exponentiation:", a ** b)
# Task 1: Predict and verify results

result1 = 5 + 3 * 2 ** 2
result2 = (5 + 3) * 2 ** 2
result3 = 10 % 3 + 5 * 2

print("Result 1 =", result1)
print("Result 2 =", result2)
print("Result 3 =", result3)

# Task 3: Unit Conversion Challenge

# Prompt the user for inches
inches = int(input("\nEnter the number of inches: "))

# Calculate feet and remaining inches
feet = inches // 12
remaining_inches = inches % 12

# Display result
print(f"{inches} inches is equal to {feet} feet and {remaining_inches} inches.")
# Prompt the user to enter a number of inches
inches = int(input("Enter the number of inches: "))

# Calculate how many feet and remaining inches
feet = inches // 12
remaining_inches = inches % 12

# Print the result in a user-friendly format
print(f"{inches} inches is equal to {feet} feet and {remaining_inches} inches.")
# Movie Ticket Price Calculator

# Step 1: Create variables
age = int(input("Enter your age: "))
is_student = input("Are you a student? (yes/no): ").lower() == "yes"

# Step 2: Set base price
base_price = 12
discount = 0

# Step 3: Apply discount rules (only the best one applies)
if age <= 12:
    discount = 3
elif age >= 65:
    discount = 4
elif is_student:
    discount = 2

# Step 4: Calculate final price
final_price = base_price - discount

# Step 5: Display the result
print(f"\nBase price: ${base_price}")
print(f"Discount: ${discount}")
print(f"Final ticket price: ${final_price}")
# Step 1: Set correct login details
username = "kyee"
password = "011105"
is_2fa_enabled = True

# Step 2: Prompt the user for their input
input_username = input("Enter username: ")
input_password = input("Enter password: ")
input_2fa_code = input("Enter 2FA code: ")

# Step 3: Correct 2FA code
correct_2fa_code = "123456"

# Step 4: Check login conditions
if (input_username == username and
    input_password == password and
    (not is_2fa_enabled or input_2fa_code == correct_2fa_code)):
    print("Login successful!")
else:
    print("Login failed!")
# Shipping Cost Calculator

# Step 1: Create variables
weight = float(input("Enter the total weight of the order (in pounds): "))
destination = input("Enter the destination (domestic/international): ").lower()
membership = input("Enter membership type (standard/premium): ").lower()

# Step 2: Base cost
base_cost = 10
extra_weight_charge = 0
international_surcharge = 0

# Step 3: Apply rules
# Add $5 if weight > 20 lbs
if weight > 20:
    extra_weight_charge = 5

# Start calculating total
total_cost = base_cost + extra_weight_charge

# Apply international rule
if destination == "international" and membership != "premium":
    total_cost *= 2  # double the cost if international and not premium

# Apply premium discount (20%) and exemption from international surcharge
if membership == "premium":
    total_cost *= 0.8  # 20% discount

# Step 4: Print detailed breakdown
print("\n===== Shipping Cost Breakdown =====")
print(f"Base shipping cost: ${base_cost:.2f}")
print(f"Extra charge for weight: ${extra_weight_charge:.2f}")

if destination == "international" and membership != "premium":
    print("International surcharge: Applied (cost doubled)")
elif destination == "international" and membership == "premium":
    print("International surcharge: Exempt (premium member)")
else:
    print("International surcharge: Not applicable")

if membership == "premium":
    print("Membership discount: 20% applied")

print("-----------------------------------")
print(f"Final shipping cost: ${total_cost:.2f}")    
