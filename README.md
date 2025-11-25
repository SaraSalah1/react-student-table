# 📝 React Student Management System

A modern React application to **manage student records**.  
Users can add, edit, delete, search, and filter students by name, semester, or department.  
The project demonstrates **React Hooks**, **dynamic table updates**, **localStorage persistence**, and **responsive UI design** with **Tailwind CSS**.

---

## 🚀 Key Features

### Student Management
- Add new students with **roll number, name, semester, and department**.
- Edit student details directly in table cells.
- Delete single or multiple selected students.
- Checkbox selection for all or individual rows.
- Persistent data saved in **localStorage**.

### Search & Filter
- Filter students dynamically by **Name**, **Semester**, or **Department**.
- Select search field from dropdown for flexible filtering.

### Responsive UI
- Clean, responsive design built with **Tailwind CSS**.
- Intuitive table layout and user-friendly form inputs.

---

## 🎨 Technology Stack

| Category | Technology | Purpose |
|----------|------------|---------|
| Frontend Framework | React.js (Hooks) | Component-based UI and state handling |
| Styling | Tailwind CSS | Responsive, modern design |
| Logic | JavaScript (ES6+) | Dynamic table updates, form handling |
| Storage | localStorage API | Persistent student data |
| UI Components | HTML5 & CSS3 | Table layout, forms, buttons |

---

## 📸 Screenshots

### Main Table View
<img src="https://github.com/user-attachments/assets/f7f0044a-8dc9-4e69-b613-ff3c14397a08" alt="Main Table View" width="600" />

### Add Student Form
<img src="https://github.com/user-attachments/assets/629ba319-a920-4609-84d4-a5c3a169a66d" alt="Add Student Form" width="600" />

### Search & Filter
<img src="https://github.com/user-attachments/assets/cd44ab8e-7edf-409f-b7bc-a7e67b22e3a1" alt="Search & Filter" width="600" />

### Delete Action
<img src="https://github.com/user-attachments/assets/07f82275-b1f7-451a-b4e4-6faeb05ef005" alt="Delete Action" width="600" />

---

## 🛠 Installation

### Clone Repository
```bash
git clone https://github.com/SaraSalah1/react-student-table.git
```

### Navigate to Project Folder
```bash
cd react-student-table
```

### Install Dependencies
```bash
# Using npm
npm install

# Using yarn
yarn install
```

### Start Development Server
```bash
# Using npm
npm start

# Using yarn
yarn start
```

### Open in Browser
```
http://localhost:3000
```

---

## 💻 Usage

### Manage Students
1. Use **input fields** to enter student name, semester, and department.  
2. Click **Add Student** to add a new record.  
3. Select students using **checkboxes** to delete single or multiple rows.  
4. Edit table cells directly for quick updates.  
5. Data updates automatically saved in **localStorage**.

### Search & Filter
1. Select a field (**Name**, **Semester**, **Department**) from the dropdown.  
2. Type the search keyword in the input field.  
3. Table dynamically filters results.

---

## 🧩 Code Snippets

### Adding a New Student
```javascript
const addRow = () => {
  if (!inputs.name) return;
  if (!inputs.semester) return;
  if (!inputs.department) return;

  let newRoll;
  do { newRoll = Math.floor(Math.random() * 10000); }
  while (rows.some((r) => r.roll === newRoll));

  setRows([...rows, { roll: newRoll, ...inputs }]);
  setInputs({ name: "", semester: "", department: "" });
};
```

### Filtering Students
```javascript
const filteredRows = rows.filter((r) =>
  r[searchBy].toLowerCase().includes(search.toLowerCase())
);
```

### Delete Selected Students
```javascript
const deleteSelected = () => {
  setRows(rows.filter((r) => !selectionModel.includes(r.roll)));
  setSelectionModel([]);
};
```

---

## 🤝 Contributing

1. Fork the repository.  
2. Create a feature branch:
```bash
git checkout -b feature/YourFeature
```
3. Commit your changes:
```bash
git commit -m "Add some feature"
```
4. Push branch:
```bash
git push origin feature/YourFeature
```
5. Open a Pull Request.

---

👩‍💻 **Author:** [Sara Salah](https://github.com/SaraSalah1)  
📦 **Project Repository:** [react-student-table](https://github.com/SaraSalah1/react-student-table)

---

## 📝 License

This project is licensed under the MIT License
