# Программа "Управления задачами" 

## Описание проекта 

Этот проект представляет собой программу на Python для управления списком задач. Пользователь может добавлять новые задачи, удалять существующие и отображать список текущих задач. 

## Ссылки 

- [Ссылка на блокнот Google Colab](https://colab.research.google.com/drive/1GifMcwIveKvfpKF7zyViLpPe-ADY-Sl8?usp=sharing) 
- [URL видео презентации проекта](ссылка) 

## Примеры кода 

python 
def add_task(tasks, new_task): 
tasks.append(new_task) 

def remove_task(tasks, task_index): 
if 1 <= task_index <= len(tasks): 
del tasks[task_index - 1] 
else: 
print("Такой задачи нет в списке!") 

def show_tasks(tasks): 
if tasks: 
print("Ваши задачи:") 
for index, task in enumerate(tasks, start=1): 
print(f"{index}. {task}") 
else: 
print("У вас пока нет задач!") 

def main(): 
todo_list = [] 

while True: 
print("\n1. Добавить задачу") 
print("2. Удалить задачу") 
print("3. Показать задачи") 
print("4. Выйти") 

choice = input("Выберите действие: ") 

if choice == "1": 
new_task = input("Введите новую задачу: ") 
add_task(todo_list, new_task) 
elif choice == "2": 
show_tasks(todo_list) 
task_index = int(input("Введите номер задачи для удаления: ")) 
remove_task(todo_list, task_index) 
elif choice == "3": 
show_tasks(todo_list) 
elif choice == "4": 
print("До свидания!") 
break 
else: 
print("Неверный вариант. Попробуйте еще раз.") 

if __name__ == "__main__": 
main()
