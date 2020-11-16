My original solution for FILE index.js




  // STEP 1
document.addEventListener("DOMContentLoaded", () => {
  // your code here

  // STEP 2
  let taskForm = document.getElementById("create-task-form");

  // console.log(form);    // <= test code with this

  let tasks = document.getElementById("tasks");

  // STEP 3
  // NOTE Click the submit (Create New Task) button to console.log test all code inside of addEventListener for submit
  taskForm.addEventListener("submit", function(e) {
    // event.preventDefault
    e.preventDefault()

    // console.log(e.target);     // <= test code to see what element/node

    // STEP 4
    let userInputTask = document.getElementById("new-task-description").value
    // console.log(userInputTask);    // <= test code to see user's input

    // moved =>   let tasks = document.getElementById("tasks");     <= moved earlier in code before event listener on submit because submit already exists on the page (in the HTML) so it does NOT need repeated call when submit is clicked [tested with below]
    // console.log(tasks);     // <= test code to see list of tasks

    // BONUS added if statement to prevent blank entries to the task list
    if (userInputTask == "") {
      alert("Please enter a task")
      return
    }

    // STEP 5
    let liTask = document.createElement("li")
    
    // console.log(liTask)    //   <= test code to see if li tag exists

    // liTask.innerText = "Text placed inside the li tag";
    // console.log(liTask);   //    <= test code with hardcoded text to see if text placed inside the li tag

    // debugger;    // <= test variables in the debugger's Source lower Console

    // STEP 6
    liTask.innerText = userInputTask

    // STEP 7
    tasks.appendChild(liTask);

    // console.log(tasks);    //  <= test final app

    // STEP 8
    taskForm.reset()

  })


  


});

