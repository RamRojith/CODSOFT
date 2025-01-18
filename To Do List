# CODSOFT
Your code is a Python-based To-Do List program with options to view tasks, add new ones, mark tasks as completed, and exit. Tasks are stored as dictionaries in a list. The program uses a menu-driven loop with input validation for smooth user interaction.

def show_menu():
    print("\n===== To-Do List Menu =====")
    print("1. View To-Do List")
    print("2. Add Task")
    print("3. Mark Task as Completed")
    print("4. Exit")

def view_tasks(tasks):
    if not tasks:
        print("\nNo tasks available.")
    else:
        print("\nYour To-Do List:")
        for index, task in enumerate(tasks, start=1):
            status = "[Completed]" if task['completed'] else "[Pending]"
            print(f"{index}. {task['task']} {status}")

def add_task(tasks):
    task = input("Enter the new task: ").strip()
    if task:
        tasks.append({"task": task, "completed": False})
        print("Task added successfully!")
    else:
        print("Task cannot be empty!")

def mark_task_completed(tasks):
    view_tasks(tasks)
    if not tasks:
        return

    try:
        task_num = int(input("Enter the task number to mark as completed: "))
        if 1 <= task_num <= len(tasks):
            tasks[task_num - 1]['completed'] = True
            print(f"Task '{tasks[task_num - 1]['task']}' marked as completed!")
        else:
            print("Invalid task number.")
    except ValueError:
        print("Please enter a valid number.")

def main():
    tasks = []
    show_menu()
    while True:
        try:
            choice = int(input("\nEnter your choice: "))

            if choice == 1:
                view_tasks(tasks)
            elif choice == 2:
                add_task(tasks)
            elif choice == 3:
                mark_task_completed(tasks)
            elif choice == 4:
                print("Goodbye!")
                break
            else:
                print("Invalid choice. Please try again.")
        except ValueError:
            print("Please enter a valid number.")

if __name__ == "__main__":
    main()


