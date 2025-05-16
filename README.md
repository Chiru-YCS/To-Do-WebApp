
# 📝 Flask TODO Application

A clean and responsive TODO list web application built using **Flask**, **SQLite**, and **Bootstrap**. This app enables users to add, update, and delete tasks, while displaying them in a structured table. It's ideal for learning the basics of Flask, templating with Jinja2, database handling with SQLAlchemy, and frontend styling with Bootstrap.

---

## 📌 Features

- ✅ Add new TODO items with title and description  
- 📄 View all existing tasks in a tabular format  
- 🛠 Update any existing TODO  
- 🗑 Delete tasks with a click  
- 📅 Automatic timestamping for each task  
- 💾 Data persistence using SQLite  
- 📱 Responsive design using Bootstrap 5  

---

## 🧰 Tech Stack

| Component  | Technology         |
|------------|--------------------|
| Language   | Python             |
| Framework  | Flask              |
| Database   | SQLite (SQLAlchemy)|
| Frontend   | HTML, Bootstrap 5  |
| Templating | Jinja2             |

---

## 🗂 Project Structure

```
.
├── app.py               # Main backend Flask application
├── todo.db              # SQLite database (auto-created)
├── templates/
│   ├── base.html        # Reusable base layout
│   ├── index.html       # Home page for viewing & adding tasks
│   └── update.html      # Page for updating existing tasks
```

---

## 🚀 Getting Started

### 📦 Prerequisites

Ensure you have Python and pip installed:

```bash
python --version
pip --version
```

### 📥 Installation

1. Clone the repository (or download manually):

```bash
git clone <repository-url>
cd <project-directory>
```

2. Install the required packages:

```bash
pip install Flask Flask-SQLAlchemy
```

3. Run the application:

```bash
python app.py
```

4. Open your browser and go to:

```
http://127.0.0.1:5000/
```

---

## 🌐 Application Routes

| Route                  | Method     | Description                            |
|------------------------|------------|----------------------------------------|
| `/`                    | GET, POST  | View all TODOs and add new ones        |
| `/update/<int:sno>`    | GET, POST  | Update an existing TODO item           |
| `/delete/<int:sno>`    | GET        | Delete a TODO item                     |
| `/show`                | GET        | Debug route to print TODOs in console  |

---

## 📁 Template Summary

### `base.html`

- Defines a basic HTML structure using Bootstrap 5.
- Includes navbar and block definitions for reuse.

### `index.html`

- Displays a form to add a new TODO (title + description).
- Lists all current TODO items in a Bootstrap table.
- Each row includes buttons for **Update** and **Delete**.

### `update.html`

- Displays a form to edit an existing TODO item.
- Pre-fills the form fields using current task data.

---

## 📸 UI Description

- **Add Section:** Simple form for entering new TODOs.
- **List Section:** Responsive table displaying:
  - Serial number
  - Title
  - Description
  - Timestamp
  - Update/Delete action buttons

Sample row:

```html
<tr>
  <th scope="row">1</th>
  <td>Buy groceries</td>
  <td>Milk, Eggs, Bread</td>
  <td>2025-05-16 10:30:00</td>
  <td>
    <a href="/update/1" class="btn btn-outline-success btn-sm">Update</a>
    <a href="/delete/1" class="btn btn-outline-danger btn-sm">Delete</a>
  </td>
</tr>
```

---

## 💡 Future Improvements

- ✅ Add task status (completed/incomplete)
- 🔍 Implement search and filter functionality
- 🔐 User authentication system
- 📈 Dashboard analytics
- 📱 Make it a Progressive Web App (PWA)

---

## 📄 License

This project is free and open-source. You may use and modify it for personal, educational, or commercial use.

---

## 🙌 Acknowledgements

- [Flask](https://flask.palletsprojects.com/)
- [SQLAlchemy](https://www.sqlalchemy.org/)
- [Bootstrap](https://getbootstrap.com/)

---

> Made with ❤️ using Flask & Bootstrap
