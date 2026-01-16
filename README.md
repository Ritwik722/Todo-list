# 📝 Minimalist FastAPI Todo App

A clean, responsive, and fully functional Todo List application built with **Python FastAPI** and **SQLite**. This project demonstrates a full-stack implementation using Server-Side Rendering (SSR) with Jinja2 templates, avoiding the need for complex frontend frameworks like React or Vue.

![Project Status](https://img.shields.io/badge/status-active-success.svg)
![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## ✨ Features

* **Create Tasks:** Add new items to your list instantly.
* **Persistent Storage:** Data is saved to a local SQLite database (`todos.db`).
* **Status Toggling:** Mark tasks as completed/active with a single click.
* **Delete Tasks:** Remove unwanted items permanently.
* **Responsive Design:** specific CSS media queries for mobile support.
* **Dark Mode UI:** A custom "Glassmorphism" aesthetic using CSS variables.

## 🛠️ Tech Stack

**Backend:**
* [FastAPI](https://fastapi.tiangolo.com/) - High-performance web framework.
* [SQLAlchemy](https://www.sqlalchemy.org/) - ORM for database interactions.
* [Jinja2](https://jinja.palletsprojects.com/) - Templating engine for HTML rendering.

**Frontend:**
* **HTML5** - Semantic markup.
* **CSS3** - Custom styling with Flexbox and CSS Variables (No Bootstrap/Tailwind).

**Database:**
* **SQLite** - Serverless, zero-configuration SQL database engine.

---

## 📂 Project Structure

To run this project correctly, ensure your files are organized exactly as shown below. `main.py` expects specific directories for templates and static files.

```text
/my-todo-app
│
├── main.py              # The entry point and backend logic
├── todos.db             # Generated automatically on first run
│
├── templates/           # Folder for HTML files
│   └── index.html       # The main UI template
│
└── static/              # Folder for CSS/Images
    └── styles.css       # The styling sheet

```

---

## 🚀 Getting Started

Follow these steps to set up the project locally.

### 1. Clone the Repository

```bash
git clone [https://github.com/your-username/fastapi-todo.git](https://github.com/your-username/fastapi-todo.git)
cd fastapi-todo

```

### 2. Create a Virtual Environment (Optional but Recommended)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Mac/Linux
python3 -m venv venv
source venv/bin/activate

```

### 3. Install Dependencies

You need `fastapi`, `uvicorn` (server), `sqlalchemy`, `jinja2`, and `python-multipart` (for form handling).

```bash
pip install fastapi uvicorn sqlalchemy jinja2 python-multipart

```

### 4. Run the Application

Start the development server using Uvicorn.

```bash
uvicorn main:app --reload

```

### 5. Open in Browser

Visit the following URL to see your app in action:
`http://127.0.0.1:8000`

---

## 📖 API & Logic Overview

The application follows a standard CRUD pattern:

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/` | Fetches all tasks from `todos.db` and renders `index.html`. |
| `POST` | `/create` | Receives form data to create a new `Todo` entry. |
| `POST` | `/update/{id}` | Updates the `completed` boolean status of a task. |
| `POST` | `/delete/{id}` | Deletes a task record by ID. |

*Code Reference:* Logic handling is located in `main.py` using `SessionLocal` for database transactions.

---

## 🎨 Design Customization

The design is handled entirely in `static/styles.css`. You can easily change the color theme by editing the CSS Variables at the top of the file:

```css
:root {
  --bg: #0f1724;       /* Main Background */
  --accent: #7c5cff;   /* Primary Button/Focus Color */
  --success: #10b981;  /* Completed Checkmark Color */
}

```

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

```

```
