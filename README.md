To-Do List Manager
1. Project Title

To-Do List Manager

2. Overview of the Project

The To-Do List Manager is a simple productivity application that allows users to add, view, update, and delete tasks.
This project helps users organize their daily activities by maintaining a list of tasks they need to complete.
It is designed for beginners to understand basic Python programming concepts such as lists, functions, conditional statements, and loops.

3. Features

✔ Add new tasks

✔ View all tasks

✔ Mark a task as completed

✔ Delete tasks

✔ User-friendly menu system

✔ Stores tasks temporarily during runtime

4. Technologies / Tools Used

Programming Language: Python

Editor/IDE: VS Code / PyCharm / IDLE / Any Python editor

Version: Python 3.x

Optional Tools:

Terminal/Command Prompt

Git (optional for version control)

5. Steps to Install & Run the Project
Step 1: Install Python

Download and install Python 3.x from the official Python website.

Step 2: Create Project Folder

Create a folder named:
ToDoListManager

Step 3: Create Python File

Inside the folder, create a file named:
todo.py

Step 4: Copy the Code

Paste the following code:

tasks = []

def add_task():
    task = input("Enter task: ")
    tasks.append({"task": task, "completed": False})
    print("Task added successfully!\n")

def view_tasks():
    if not tasks:
        print("No tasks available.\n")
        return
    print("\nYour Tasks:")
    for i, t in enumerate(tasks, 1):
        status = "✔ Completed" if t["completed"] else "✘ Not Completed"
        print(f"{i}. {t['task']} - {status}")
    print()

def mark_completed():
    view_tasks()
    try:
        num = int(input("Enter task number to mark as completed: "))
        tasks[num - 1]["completed"] = True
        print("Task marked as completed!\n")
    except:
        print("Invalid choice!\n")

def delete_task():
    view_tasks()
    try:
        num = int(input("Enter task number to delete: "))
        tasks.pop(num - 1)
        print("Task deleted successfully!\n")
    except:
        print("Invalid choice!\n")

def menu():
    while True:
        print("==== TO-DO LIST MANAGER ====")
        print("1. Add Task")
        print("2. View Tasks")
        print("3. Mark Task as Completed")
        print("4. Delete Task")
        print("5. Exit")
        choice = input("Enter your choice: ")

        if choice == '1':
            add_task()
        elif choice == '2':
            view_tasks()
        elif choice == '3':
            mark_completed()
        elif choice == '4':
            delete_task()
        elif choice == '5':
            print("Exiting... Goodbye!")
            break
        else:
            print("Invalid option! Try again.\n")

menu()

Step 5: Run the Project

Open terminal/cmd

Navigate to project folder

Run the command:

python todo.py

6. Instructions for Testing

Perform the following tests to verify the project works:

Test Case 1 — Add a Task

Input: “Buy groceries”

Expected Result: Task added to the list

Test Case 2 — View Tasks

After adding tasks, view the list

Expected Result: Tasks display with correct numbering

Test Case 3 — Mark as Completed

Select any task number

Expected Result: Status changes to “✔ Completed”

Test Case 4 — Delete a Task

Delete any task

Expected Result: Removed from list

Test Case 5 — Exit

Select option 5

Expected Result: Program terminates successfully

7. Screenshots (Optional but Recommended)

(You can paste screenshots here after running your program)

Example placeholders:

Screenshot 1: Adding tasks

Screenshot 2: Viewing tasks

Screenshot 3: Marking a task as completed

Screenshot 4: Deleting tasks
