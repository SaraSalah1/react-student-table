# 📝 Student Management Table

A modern React application to manage student records. Users can add, edit, delete, search, and filter students by name, semester, or department. The project demonstrates React hooks, dynamic table updates, localStorage persistence, and responsive UI design with Tailwind CSS.

---

## 🚀 Features

- Add new students with roll, name, semester, and department.
- Edit student details directly in the table.
- Delete single or multiple selected students.
- Search and filter students by Name, Semester, or Department.
- Select all/individual students using checkboxes.
- Persistent data stored in browser localStorage.
- Responsive design with Tailwind CSS.

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
<img src="https://github.com/user-attachments/assets/f7f0044a-8dc9-4e69-b613-ff3c14397a08"   alt="ChatGPT Dropdown" width="600" />

*Shows all students with editable fields and checkboxes for selection.*

### 2. Add Student Form
<img src="https://github.com/user-attachments/assets/629ba319-a920-4609-84d4-a5c3a169a66d"   alt="Login/Signup Modal" width="600" />

*Input fields to add new student records dynamically.*

### 3. Search and Filter
<img src="https://github.com/user-attachments/assets/cd44ab8e-7edf-409f-b7bc-a7e67b22e3a1"   alt="Landing Page / Chat Input" width="600" />

*Dropdown to select search criteria and input field to filter students.*

### 4. Delete Action
<img src="https://github.com/user-attachments/assets/07f82275-b1f7-451a-b4e4-6faeb05ef005"   alt="Help Menu" width="600" />

*Delete single or multiple students directly from the table.*


---

## 🛠 Installation & Run

- ### Clone the repository

  git clone https://github.com/SaraSalah1/react-student-table.git


- ### Navigate to the project folder
      cd react-student-table

- ### Install dependencies
      npm install

- ### Start the development server
      npm start

- ### Open in your browser
      http://localhost:3000

    ---

## 💻 Usage

- Use input fields at the top to add a new student.

- Use checkboxes to select single or multiple students.

- Click Add Student to add a new record.

- Click Delete Selected to remove all selected students.

- Use the dropdown to select a search field (Name, Semester, Department) and filter students dynamically.

- Edit student information directly in the table cells.

- Table updates are saved automatically in localStorage.
   ---

##🧩 Code Snippets

Adding a New Student

```
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

Filtering Students

```
const filteredRows = rows.filter((r) =>
  r[searchBy].toLowerCase().includes(search.toLowerCase())
);

```

---

## 🤝 Contributing

Contributions are welcome! Follow these steps:

- #### Fork the repository

- #### Create a feature branch

      git checkout -b feature/YourFeature


- #### Commit your changes

      git commit -m "Add some feature"


- #### Push to the branch

      git push origin feature/YourFeature
  
- #### Open a Pull Request

- ---

👩‍💻 **Created by [Sara Salah](https://github.com/SaraSalah1)**  
📦 [View the project on GitHub](https://github.com/SaraSalah1/react-student-table)

---

## 📝 License

This project is licensed under the MIT License
