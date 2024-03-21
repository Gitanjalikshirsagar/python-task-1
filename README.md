def add_task(tasks, task):
    tasks.append(task)
    print("Task added successfully!")

def remove_task(tasks, task):
    if task in tasks:
        tasks.remove(task)
        print("Task removed successfully!")
    else:
        print("Task not found in the list.")

def view_tasks(tasks):
    if tasks:
        print("Your To-Do List:")
        for index, task in enumerate(tasks, start=1):
            print(f"{index}. {task}")
    else:
        print("Your To-Do List is empty.")

def main():
    tasks = []

    while True:
        print("\n----To-Do List Menu----")
        print("1. Add Task")
        print("2. Remove Task")
        print("3. View Tasks")
        print("4. Exit")

        choice = input("Enter your choice: ")

        if choice == '1':
            task = input("Enter task to add: ")
            add_task(tasks, task)
        elif choice == '2':
            task = input("Enter task to remove: ")
            remove_task(tasks, task)
        elif choice == '3':
            view_tasks(tasks)
        elif choice == '4':
            print("Exiting program...")
            break
        else:
            print("Invalid choice. Please enter a valid option.")

if __name__ == "__main__":
    main()
