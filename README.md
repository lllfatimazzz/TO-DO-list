# Simple To-Do List App

def show_menu():
    print("\n--- To-Do List Menu ---")
    print("1. View To-Do List")
    print("2. Add Task")
    print("3. Remove Task")
    print("4. Exit")
    
def view_tasks(tasks):
    if not tasks:
        print("\nNo tasks in your to-do list.")
    else:
        print("\nYour To-Do List:")
        for idx, task in enumerate(tasks, 1):
            print(f"{idx}. {task}")

def add_task(tasks):
    task = input("Enter the task: ")
    tasks.append(task)
    print(f"Task '{task}' added successfully!")

def remove_task(tasks):
    view_tasks(tasks)
    try:
        task_num = int(input("\nEnter the task number to remove: "))
        if 1 <= task_num <= len(tasks):
            removed_task = tasks.pop(task_num - 1)
            print(f"Task '{removed_task}' removed successfully!")
        else:
            print("Invalid task number.")
    except ValueError:
        print("Please enter a valid number.")

def main():
    tasks = []
    while True:
        show_menu()
        choice = input("Choose an option (1-4): ")
        
        if choice == '1':
            view_tasks(tasks)
        elif choice == '2':
            add_task(tasks)
        elif choice == '3':
            remove_task(tasks)
        elif choice == '4':
            print("Exiting the To-Do List App. Goodbye!")
            break
        else:
            print("Invalid choice. Please select a valid option.")

if _name_ == "_main_":
    main()


    # Simple To-Do List App

A command-line interface (CLI) application that allows you to manage your daily tasks. You can add, view, and remove tasks easily with this Python-based To-Do List App.

## Features

- *View To-Do List*: Displays all tasks currently in the to-do list.
- *Add Task*: Allows users to add a new task to the list.
- *Remove Task*: Removes a task from the list based on its number.
- *Exit*: Exits the application gracefully.


    
## Usage

Upon running the script, you'll see the following menu:

- *View To-Do List*: Displays all tasks in the list.
- *Add Task*: You can add a new task by entering the task name.
- *Remove Task*: You can remove a task by specifying its number from the displayed list.
- *Exit*: Exits the application.

