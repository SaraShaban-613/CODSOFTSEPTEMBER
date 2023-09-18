class to_do_items:
    def __init__(self, task):
        self.task = task
        self.completed = False

class to_do_list:
    def __init__(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append(to_do_items(task))
        print("Task added!")

    def mark_completed(self, index):
        if 0 <= index < len(self.tasks):
            self.tasks[index].completed = True
            print("Task marked as completed!")
        else:
            print("Invalid task index.")

    def show_tasks(self):
        if not self.tasks:
            print("No tasks in the list.")
        else:
            print("Tasks:")
            for index, task_item in enumerate(self.tasks):
                status = "Done" if task_item.completed else "Not Done"
                print(f"{index+1}. {task_item.task} - {status}")

def main():
    todo_list = to_do_list()

    while True:
        print("\nMenu:")
        print("1. Add Task")
        print("2. Mark Task as Completed")
        print("3. Show Tasks")
        print("4. Exit")
        choice = input("Enter your choice: ")

        if choice == "1":
            task = input("Enter task description: ")
            todo_list.add_task(task)
        elif choice == "2":
            index = int(input("Enter task index to mark as completed: ")) - 1
            todo_list.mark_completed(index)
        elif choice == "3":
            todo_list.show_tasks()
        elif choice == "4":
            print("Exiting...")
            break
        else:
            print("Invalid choice. Please select again.")

if __name__ == "__main__":
    main()
