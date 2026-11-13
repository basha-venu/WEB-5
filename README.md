# Exp 05 – React Lab Exercise: Form Handling in React

## NAME : BASHA VENU

## REG NO : 2305001005

## Aim

To develop a simple Student Registration Form using React and handle form input values using the `useState` Hook.

## Objectives

- To create a form using React.
- To create input fields such as Name, Register Number, and Department.
- To use `useState()` to store form data.
- To handle input changes using `onChange`.
- To handle form submission using `onSubmit`.
- To display submitted student details.

## Program

### Step 1 – Create React Project

```bash
npm create vite@latest react-form
cd react-form
npm install
npm run dev
```

Select React as the framework and JavaScript as the variant.

### Step 2 – App.jsx

```

import { useState } from "react";
import "./App.css";

function App() {
  const [name, setName] = useState("");
  const [registerNo, setRegisterNo] = useState("");
  const [department, setDepartment] = useState("");

  const handleSubmit = (event) => {
    event.preventDefault();

    alert(
      "Name: " + name +
      "\nRegister Number: " + registerNo +
      "\nDepartment: " + department
    );
  };

  return (
    <div className="container">
      <h1>Student Registration Form</h1>

      <form onSubmit={handleSubmit}>
        <label>Name:</label>
        <input
          type="text"
          value={name}
          onChange={(event) => setName(event.target.value)}
          placeholder="Enter your name"
          required
        />

        <label>Register Number:</label>
        <input
          type="text"
          value={registerNo}
          onChange={(event) => setRegisterNo(event.target.value)}
          placeholder="Enter register number"
          required
        />

        <label>Department:</label>
        <input
          type="text"
          value={department}
          onChange={(event) => setDepartment(event.target.value)}
          placeholder="Enter department"
          required
        />

        <button type="submit">Submit</button>
      </form>
    </div>
  );
}

export default App;

```

### Step 3 – App.css

```
.container {
  width: 400px;
  margin: 50px auto;
  padding: 25px;
  border: 1px solid gray;
  border-radius: 10px;
}

h1 {
  text-align: center;
  color: blue;
}

label {
  display: block;
  margin-top: 15px;
  font-weight: bold;
}

input {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  box-sizing: border-box;
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: blue;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

```

## Output

### Entered Student Details
<img width="1107" height="582" alt="image" src="https://github.com/user-attachments/assets/5d33f97b-9cf5-4e06-8974-81d8e623bedb" />

### Submitted Details – Alert Box
<img width="1360" height="712" alt="image" src="https://github.com/user-attachments/assets/0f039ff5-2363-46c3-bf22-567b92139ab4" />



## Result

Thus, a Student Registration Form was successfully created using React. Form input values were managed using the `useState()` Hook, input changes were handled using `onChange`, and form submission was handled using `onSubmit`. The submitted student details were successfully displayed using an alert box.
