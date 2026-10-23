# Student Grade Calculator
# Created by Gobika

print("=== Student Grade Calculator ===")

name = input("Enter student name: ")

marks = []

for i in range(1, 6):
    mark = float(input(f"Enter marks for subject {i} (0-100): "))

    if mark < 0 or mark > 100:
        print("Invalid marks! Enter a value between 0 and 100.")
        exit()

    marks.append(mark)

total = sum(marks)
average = total / len(marks)

if average >= 90:
    grade = "A+"
elif average >= 80:
    grade = "A"
elif average >= 70:
    grade = "B"
elif average >= 60:
    grade = "C"
elif average >= 50:
    grade = "D"
else:
    grade = "F"

print("\n=== Student Result ===")
print("Student Name:", name)
print("Total Marks:", total, "/ 500")
print(f"Average: {average:.2f}%")
print("Grade:", grade)

if average >= 50:
    print("Result: PASS")
else:
    print("Result: FAIL")

print("\nThank you for using the calculator!")
