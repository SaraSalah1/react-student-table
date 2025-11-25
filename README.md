# 📝 React Student Management Table

A modern React application for **managing student records**.  
Users can **add, edit, delete, search, and filter students** by Name, Semester, or Department.  
The project demonstrates **React Hooks**, **dynamic table updates**, **localStorage persistence**, and **responsive UI** with Tailwind CSS.

---

## 🚀 Features

- Add new students with Roll Number, Name, Semester, and Department  
- Edit student details directly in the table  
- Delete single or multiple selected students  
- Search and filter students by Name, Semester, or Department  
- Select all or individual students using checkboxes  
- Persistent data stored in browser **localStorage**  
- Fully responsive design using **Tailwind CSS**  

---

## 🎨 Technologies Used

- **React.js**  
- **JavaScript (ES6)**  
- **Tailwind CSS**  
- **HTML5 & CSS3**  
- **localStorage API**  

---

## 📸 Screenshots

### 1. Main Table View
<img src="https://github.com/user-attachments/assets/f7f0044a-8dc9-4e69-b613-ff3c14397a08" width="600" />

*Displays all students with editable fields and selection checkboxes.*

### 2. Add Student Form
<img src="https://github.com/user-attachments/assets/629ba319-a920-4609-84d4-a5c3a169a66d" width="600" />

*Input fields to add new student records dynamically.*

### 3. Search and Filter
<img src="https://github.com/user-attachments/assets/cd44ab8e-7edf-409f-b7bc-a7e67b22e3a1" width="600" />

*Select search criteria and filter students in real-time.*

### 4. Delete Action
<img src="https://github.com/user-attachments/assets/07f82275-b1f7-451a-b4e4-6faeb05ef005" width="600" />

*Delete single or multiple students directly from the table.*

---

## 🛠 Installation & Run

### 1. Clone the repository
```bash
git clone https://github.com/SaraSalah1/react-student-table.git
```

### 2. Navigate to the project folder
```bash
cd react-student-table
```

### 3. Install dependencies
#### Using npm:
```bash
npm install
```
#### Using yarn:
```bash
yarn install
```

### 4. Start the development server
#### Using npm:
```bash
npm start
```
#### Using yarn:
```bash
yarn start
```

### 5. Open in your browser
```
http://localhost:3000
```

---

## 💻 Usage

- Fill in the input fields to add a new student.  
- Use checkboxes to select single or multiple students.  
- Click **Add Student** to create a new record.  
- Click **Delete Selected** to remove selected students.  
- Select a search field (Name, Semester, Department) from the dropdown and filter students dynamically.  
- Edit student information directly in table cells.  
- All updates are saved automatically in **localStorage**.

---

## 🧩 Code Snippets

### ➕ Adding a New Student
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

### 🔍 Filtering Students
```javascript
const filteredRows = rows.filter((r) =>
  r[searchBy].toLowerCase().includes(search.toLowerCase())
);
```

---

## 🤝 Contributing

Contributions are welcome!  

1. Fork the repository  
2. Create a feature branch:
```bash
git checkout -b feature/YourFeature
```
3. Commit your changes:
```bash
git commit -m "Add some feature"
```
4. Push the branch:
```bash
git push origin feature/YourFeature
```
5. Open a Pull Request  

---

👩‍💻 **Created by [Sara Salah](https://github.com/SaraSalah1)**  
📦 **Project Repository:** [react-student-table](https://github.com/SaraSalah1/react-student-table)

---

## 📝 License

This project is licensed under the **MIT License**.
