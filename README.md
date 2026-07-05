# COS202 Personal Pocket CGPA Calculator (PPC)

print("========================================")
print("   PERSONAL POCKET CGPA CALCULATOR")
print("========================================")

num_courses = int(input("Enter the number of courses: "))

total_points = 0
total_units = 0

for i in range(1, num_courses + 1):
    print("\nCourse", i)

    course = input("Course Title: ")
    unit = int(input("Course Unit: "))
    grade = input("Grade (A-F): ").upper()

    if grade == "A":
        point = 5
    elif grade == "B":
        point = 4
    elif grade == "C":
        point = 3
    elif grade == "D":
        point = 2
    elif grade == "E":
        point = 1
    elif grade == "F":
        point = 0
    else:
        print("Invalid Grade!")
        point = 0

    quality_point = point * unit

    total_points += quality_point
    total_units += unit

if total_units > 0:
    cgpa = total_points / total_units

    print("\n========================================")
    print("TOTAL COURSE UNITS :", total_units)
    print("TOTAL GRADE POINTS :", total_points)
    print("YOUR CGPA IS :", round(cgpa, 2))

    if cgpa >= 4.50:
        print("CLASS OF DEGREE: First Class")
    elif cgpa >= 3.50:
        print("CLASS OF DEGREE: Second Class Upper")
    elif cgpa >= 2.40:
        print("CLASS OF DEGREE: Second Class Lower")
    elif cgpa >= 1.50:
        print("CLASS OF DEGREE: Third Class")
    elif cgpa >= 1.00:
        print("CLASS OF DEGREE: Pass")
    else:
        print("CLASS OF DEGREE: Fail")

print("========================================")
print("Thank you for using PPC!")