# Python-Basic-Project
**Python Student Management Program with add, view, and sort features**

students = []  
 
##### Adding student 
def add_student():
    name = input("Enter student name: ")
    score = int(input("Enter student score: "))
    student = {"name": name, "score": score}
    students.append(student)
    print("Student Successfully added!")
 
##### viewing students
def view_students():
    if not students:
        print("No students yet.")
        return
    print("\n--- Student List ---")
    for s in students:
        result = "Pass" if s["score"] >= 40 else "Fail"
        print(f"{s['name']} - Score: {s['score']} - {result}")
    print("--------------------")
 
##### Sorting students
def sort_students():
    students.sort(key=lambda x: x["score"], reverse=True)
    print("Students sorted by score (high to low)!")
 

def main():
    while True:
        print("\n===== MENU =====")
        print("1. Add Student")
        print("2. View Students")
        print("3. Sort Students by Score")
        print("4. Exit")
        
        choice = input("Choose option: ")
        
        if choice == "1":
            add_student()
        elif choice == "2":
            view_students()
        elif choice == "3":
            sort_students()
        elif choice == "4":
            print("Exiting program. Bye!")
            break
        else:
            print("Invalid choice, try again!")
 
 
main()

#Here is our basic python program
