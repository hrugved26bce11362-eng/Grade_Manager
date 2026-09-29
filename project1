
# This dictionary stores all student data.
students = {}


def add_student():
    """Add a new student to the system."""
    name = input("Enter student name: ").strip()

    if not name:
        print("Student name cannot be empty.\n")
        return

    if name in students:
        print(name + " already exists. Please use the update option.\n")
        return

    marks_input = input("Enter marks separated by spaces: ").strip()
    if not marks_input:
        print("Please enter at least one mark.\n")
        return

    try:
        marks = [int(mark) for mark in marks_input.split()]
    except ValueError:
        print("Marks must be numbers separated by spaces.\n")
        return

    students[name] = marks
    print("Added " + name + " with marks " + str(marks) + ".\n")


def view_all_students():
    """Show all students and their average marks."""
    if not students:
        print("No students added yet.\n")
        return

    print("\n--- All Students ---")
    for name, marks in students.items():
        average = calculate_average(marks)
        print(name + ": marks=" + str(marks) + ", average=" + format(average, ".2f"))
    print()


def calculate_average(marks):
    """Return the average of a list of marks."""
    if not marks:
        return 0.0
    return sum(marks) / len(marks)


def find_topper():
    """Find the student with the highest average."""
    if not students:
        print("No students added yet.\n")
        return

    topper_name = None
    topper_average = -1

    for name, marks in students.items():
        average = calculate_average(marks)
        if average > topper_average:
            topper_average = average
            topper_name = name

    print("Topper: " + str(topper_name) + " with average " + format(topper_average, ".2f") + "\n")


def find_lowest_scorer():
    """Find the student with the lowest average."""
    if not students:
        print("No students added yet.\n")
        return

    lowest_name = None
    lowest_average = None

    for name, marks in students.items():
        average = calculate_average(marks)
        if lowest_average is None or average < lowest_average:
            lowest_average = average
            lowest_name = name

    print("Lowest scorer: " + str(lowest_name) + " with average " + format(lowest_average, ".2f") + "\n")


def update_marks():
    """Update marks for an existing student."""
    name = input("Enter student name to update: ").strip()

    if name not in students:
        print(name + " not found.\n")
        return

    marks_input = input("Enter new marks separated by spaces: ").strip()
    if not marks_input:
        print("Please enter at least one mark.\n")
        return

    try:
        marks = [int(mark) for mark in marks_input.split()]
    except ValueError:
        print("Marks must be numbers separated by spaces.\n")
        return

    students[name] = marks
    print("Updated " + name + "'s marks to " + str(marks) + ".\n")


def remove_student():
    """Delete a student from the system."""
    name = input("Enter student name to remove: ").strip()

    if name in students:
        del students[name]
        print("Removed " + name + ".\n")
    else:
        print(name + " not found.\n")


def show_menu():
    """Display the main menu."""
    print("===== STUDENT GRADE MANAGER =====")
    print("1. Add student")
    print("2. View all students")
    print("3. Find topper")
    print("4. Find lowest scorer")
    print("5. Update a student's marks")
    print("6. Remove a student")
    print("7. Exit")


def main():
    """Run the student management program."""
    while True:
        show_menu()
        choice = input("Enter your choice (1-7): ").strip()

        if choice == "1":
            add_student()
        elif choice == "2":
            view_all_students()
        elif choice == "3":
            find_topper()
        elif choice == "4":
            find_lowest_scorer()
        elif choice == "5":
            update_marks()
        elif choice == "6":
            remove_student()
        elif choice == "7":
            print("Goodbye!")
            break
        else:
            print("Invalid choice. Please enter a number from 1 to 7.\n")


main()