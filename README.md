# 🚀 CodeQuest Academy

**Learn → Build → Run → Create**

CodeQuest Academy is an interactive, project-based programming course that teaches:

* 🐍 Python
* 🌐 HTML
* 🎨 CSS
* ⚡ JavaScript
* ⚛️ React
* 🗄️ SQL
* 🚀 Full-Stack Application Architecture

The goal is simple: **don't just read code — write it, run it, experiment with it, and build something real.**

---

## ✨ Features

### 🎮 Gamified Learning

* XP system
* Levels
* Mission-based learning
* Progress tracking
* Mission completion
* Confetti and animations
* Interactive coding challenges
* Persistent progress using `localStorage`

### 💻 Real Code Execution

CodeQuest isn't just a fake code preview.

Depending on the lesson, code can actually run inside the browser.

| Technology    | Execution                          |
| ------------- | ---------------------------------- |
| HTML          | ✅ Real browser sandbox             |
| CSS           | ✅ Real CSS rendering               |
| JavaScript    | ✅ Real JavaScript sandbox          |
| React         | ✅ React + ReactDOM + Babel         |
| Python        | ✅ Pyodide                          |
| SQL           | ✅ SQLite through sql.js            |
| Final Project | ✅ Interactive project architecture |

---

## 🐍 Python

Python lessons introduce:

1. Printing
2. Variables
3. Functions
4. Conditions
5. Lists

Python code is executed directly in the browser using **Pyodide**.

Example:

```python
def greet(name):
    return "Hello " + name

print(greet("CodeQuest"))
```

---

## 🌐 HTML

Students learn how to create web pages using:

* Headings
* Paragraphs
* Forms
* Inputs
* Buttons
* Semantic HTML
* Page structure

Example:

```html
<h1>My Task Manager</h1>

<p>Welcome to my application!</p>

<button>Add Task</button>
```

HTML is rendered inside a sandboxed iframe.

---

## 🎨 CSS

Students learn:

* Colors
* Spacing
* Cards
* Borders
* Border radius
* Flexbox
* Responsive design
* Mobile layouts

Example:

```css
.card {
  padding: 20px;
  border-radius: 15px;
  background: white;
}
```

---

## ⚡ JavaScript

Students learn how to make websites interactive.

Topics include:

* Variables
* Events
* Arrays
* `map()`
* Async programming
* `fetch()`

Example:

```javascript
const button = document.querySelector("button");

button.addEventListener("click", () => {
    button.textContent = "✓ Added!";
});
```

JavaScript runs inside an isolated browser sandbox.

---

## ⚛️ React

React lessons teach:

* Components
* Props
* State
* Events
* Forms
* Application architecture

Example:

```jsx
function App() {

    const [count, setCount] =
        React.useState(0);

    return (
        <button
            onClick={() => setCount(count + 1)}
        >
            Clicked {count} times
        </button>
    );
}
```

The course loads React, ReactDOM and Babel when React execution is requested.

---

## 🗄️ SQL

Students learn relational databases through real SQLite execution.

Topics include:

* `CREATE TABLE`
* `INSERT`
* `SELECT`
* `UPDATE`
* `DELETE`
* `JOIN`

Example:

```sql
SELECT *
FROM tasks;
```

The SQL engine runs inside the browser using `sql.js`.

---

# 🚀 Final Project

The final mission combines everything.

Students build a **Task Manager** based on this architecture:

```text
          React
            │
            ▼
       JavaScript
            │
            ▼
        Python API
            │
            ▼
       SQL Database
```

The application can eventually support:

* Create tasks
* Read tasks
* Update tasks
* Delete tasks
* Mark tasks complete
* User accounts
* Multiple users
* Database relationships

This introduces students to the fundamentals of **full-stack development**.

---

# 📁 Project Structure

The course itself can be extremely simple:

```text
CodeQuest/
│
├── index.html
└── README.md
```

Everything in the course UI is contained in:

```text
index.html
```

No frontend framework is required to run the course itself.

---

# ▶️ Running the Course

## Option 1 — Open Directly

Download or clone the project and open:

```text
index.html
```

in a modern browser.

---

## Option 2 — Local Server

For the most reliable experience, run a local web server.

For example:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

---

# 🌐 Internet Requirement

The core interface is contained in the single HTML file.

However, some programming runtimes are loaded from CDNs when needed:

* Python → Pyodide
* React → React / ReactDOM / Babel
* SQL → sql.js

Therefore, **Python, React and SQL execution require an internet connection when their runtime is loaded.**

HTML, CSS and JavaScript browser execution do not require those external programming runtimes.

---

# 💾 Progress

CodeQuest saves learning progress in the browser using:

```javascript
localStorage
```

This includes:

* XP
* Level
* Completed missions
* Current mission
* Language preference

Progress is therefore retained when the student returns to the same browser.

---

# 🌍 Languages

The application supports:

* 🇬🇧 English
* 🇦🇪 Arabic

The interface automatically switches between:

```text
LTR
```

and:

```text
RTL
```

when changing languages.

Code itself remains in English because programming syntax is conventionally written in English.

---

# 🎙️ Voice Learning

CodeQuest uses the browser's Web Speech API to provide optional lesson narration.

Students can:

* ▶ Listen
* ⏸ Pause
* ▶ Resume
* ■ Stop
* Adjust narration speed

Voice availability depends on the student's browser and installed voices.

---

# ⌨️ Keyboard Shortcuts

### Run Code

```text
Ctrl + Enter
```

Windows/Linux

or

```text
Cmd + Enter
```

Mac

### Indent Code

Press:

```text
Tab
```

inside the editor.

### Submit Challenge

Press:

```text
Enter
```

inside the challenge answer box.

---

# 🧠 Learning Philosophy

CodeQuest follows a simple learning loop:

```text
LEARN
  ↓
UNDERSTAND
  ↓
WRITE
  ↓
RUN
  ↓
BREAK
  ↓
FIX
  ↓
BUILD
```

Making mistakes is part of the course.

Students should be encouraged to change the code and see what happens.

---

# 🎯 Course Roadmap

```text
🐍 Python
   ↓
🌐 HTML
   ↓
🎨 CSS
   ↓
⚡ JavaScript
   ↓
⚛️ React
   ↓
🗄️ SQL
   ↓
🚀 Full-Stack Project
```

The progression moves from programming fundamentals toward building complete applications.

---

# 🔐 Security

User HTML and JavaScript are executed inside sandboxed browser environments rather than directly in the main CodeQuest page.

The application should **never execute arbitrary student code on a server without additional security controls**.

Python and SQL execution are also performed in the browser.

For a production version with server-side execution, additional isolation would be required, such as:

* Containers
* Resource limits
* Network restrictions
* Process isolation
* Execution timeouts
* Memory limits
* Authentication
* Server-side validation

---

# 🛠️ Technologies

The course uses:

* HTML5
* CSS3
* JavaScript
* Web Speech API
* Web Storage API
* iframe sandboxing
* React
* ReactDOM
* Babel
* Pyodide
* sql.js

---

# 💡 Future Features

Possible future versions could add:

### 🏆 Achievements

```text
🏅 First Program
🏅 HTML Builder
🏅 CSS Artist
🏅 JavaScript Explorer
🏅 React Builder
🏅 SQL Master
🏅 Full-Stack Creator
```

### 🧩 Project Builder

Students could create projects from scratch instead of only editing lesson examples.

### 📂 Multi-File Editor

For example:

```text
my-app/
│
├── index.html
├── style.css
├── script.js
│
└── README.md
```

### 🐍 Python Projects

Students could build:

* Calculator
* Quiz
* Expense tracker
* Text adventure
* AI utility

### 🌐 Web Projects

Students could build:

* Portfolio
* Landing page
* To-do list
* Weather application
* Recipe application

### ⚛️ React Projects

Students could build:

* Task manager
* Dashboard
* Habit tracker
* Notes application
* Mini SaaS interface

### 🗄️ Database Projects

Students could learn:

```text
Users
  │
  ├── Tasks
  │
  ├── Projects
  │
  └── Notes
```

---

# 🚀 Vision

CodeQuest Academy is designed around one idea:

> **Programming becomes much more exciting when you're building something you can actually use.**

Instead of spending the entire course watching tutorials, students progressively move from:

```text
"I don't understand code."
```

to:

```text
"I can write code."
```

then:

```text
"I can run code."
```

and eventually:

```text
"I can build an application."
```

---

## 📜 License

Add your preferred license here.

For example:

```text
MIT License
```

if you decide to release the project as open source.
