# ToDo-List-APP
fun main() {
    val toDoList = mutableListOfString()

    while (true) {
        printMenu()
        val choice = readLine().toIntOrNull()

        when (choice) {
            1 - addItem(toDoList)
            2 - showList(toDoList)
            3 - break
            else - println(Invalid choice. Please try again.)
        }
    }
}

fun printMenu() {
    println(n===== To-Do List =====)
    println(1. Add Item)
    println(2. Show List)
    println(3. Exit)
    print(Enter your choice )
}

fun addItem(list MutableListString) {
    print(Enter the task )
    val task = readLine()
    task.let {
        list.add(it)
        println(Task added $it)
    }  println(Invalid task. Please try again.)
}

fun showList(list ListString) {
    if (list.isEmpty()) {
        println(To-Do list is empty.)
    } else {
        println(n=== To-Do List ===)
        list.forEachIndexed { index, task -
            println(${index + 1}. $task)
        }
    }
}
