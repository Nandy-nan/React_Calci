# Ex04 Simple Calculator - React Project
## Date: 17-09-2025

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
```
APP.JS
import React, { useState } from "react";
import "./App.css";

function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleEqual = () => {
    try {
      setInput(eval(input).toString()); // Caution: eval is not safe in real apps
    } catch {
      setInput("Error");
    }
  };

  return (
    <>
      <div className="calculator">
        <h1>React Calculator</h1>
        <input type="text" value={input} readOnly />

        <div className="buttons">
          <button onClick={handleClear}>C</button>
          <button onClick={() => handleClick("/")}>/</button>
          <button onClick={() => handleClick("*")}>*</button>
          <button onClick={() => handleClick("-")}>-</button>

          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button onClick={() => handleClick("+")}>+</button>

          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button onClick={handleEqual} className="equal">=</button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>

          <button onClick={() => handleClick("0")} className="zero">0</button>
          <button onClick={() => handleClick(".")}>.</button>
        </div>
      </div>

      <footer className="footer">
        <p>&copy;Jeslin Gnanasheela M(212222040062)</p>
      </footer>
    </>
  );
}

export default App;
```
APP.CSS
```
body {
  font-family: Arial, sans-serif;
  background-color: #eef2f3;
  margin: 0;
  padding-bottom: 60px;
}

.calculator {
  width: 300px;
  margin: 60px auto;
  background: #fff;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.1);
  text-align: center;
}

h1 {
  margin-bottom: 20px;
  font-size: 24px;
}

input {
  width: 100%;
  padding: 15px;
  font-size: 20px;
  margin-bottom: 15px;
  border: 1px solid #ccc;
  border-radius: 10px;
  text-align: right;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 18px;
  background-color: #007bff;
  border: none;
  color: white;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #0056b3;
}

button.equal {
  grid-row: span 2;
  background-color: #28a745;
}

button.equal:hover {
  background-color: #1e7e34;
}

button.zero {
  grid-column: span 2;
}

.footer {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background: #ffffff;
  text-align: center;
  padding: 10px;
  font-size: 14px;
  color: #666;
  border-top: 1px solid #ddd;
  box-shadow: 0 -1px 5px rgba(0, 0, 0, 0.1);
}



```



## OUTPUT
<img width="624" height="414" alt="image" src="https://github.com/user-attachments/assets/fbad6667-e8b0-4d73-adac-3e35e70eee50" />

<img width="491" height="436" alt="image" src="https://github.com/user-attachments/assets/ddb1f242-27e0-4196-b142-2eaae6a408fd" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
