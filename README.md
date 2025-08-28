# TO-DO-LIST
1. What is a To-Do List?

A to-do list is a simple app or feature where you can:

Add tasks (things you want to do).

Mark them as completed.

Delete tasks if not needed.

Sometimes edit tasks, or even save them for later use (using local storage or a database).

👉 It’s one of the most common beginner projects because it covers basics of frontend development (HTML, CSS, JavaScript) and can later include backend (Node.js, databases, APIs).

2. What Technologies Are Used (HTML + JavaScript)?

When building a to-do list app in web development, you mainly use:

🔹 HTML (Structure)

Creates the layout of the app.

Example: Input box for adding a task, a button to submit, and a list to show tasks.
<input type="text" id="taskInput" placeholder="Enter task">
<button id="addBtn">Add Task</button>
<ul id="taskList"></ul>

🔹 CSS (Style)

Makes the to-do list look good (colors, fonts, spacing).

Example: Green check marks for completed tasks, strike-through effect.

🔹 JavaScript (Functionality)

Handles the logic:

Adding tasks to the list.

Deleting tasks.

Marking tasks as completed.

Saving tasks in Local Storage so they don’t disappear after refresh.

Example (basic logic):
const addBtn = document.getElementById("addBtn");
const taskInput = document.getElementById("taskInput");
const taskList = document.getElementById("taskList");

addBtn.addEventListener("click", () => {
  const taskText = taskInput.value.trim();
  if (taskText !== "") {
    let li = document.createElement("li");
    li.textContent = taskText;

    // mark task as done on click
    li.addEventListener("click", () => li.classList.toggle("completed"));

    // delete button
    let delBtn = document.createElement("button");
    delBtn.textContent = "❌";
    delBtn.onclick = () => li.remove();

    li.appendChild(delBtn);
    taskList.appendChild(li);
    taskInput.value = "";
  }
});


🔹 Extra Features You Can Add

Local Storage → to save tasks.

Frameworks (React, Vue, Angular) → for bigger apps.

Backend (Node.js + Database like MongoDB/MySQL) → if you want tasks to sync online.

👉 So, a basic To-Do List only needs HTML + CSS + JavaScript, but advanced versions can use React + APIs + databases.
