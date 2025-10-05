# Working with PyCharm | Run | Debug | Trace | .py File


In this lecture, we will learn how to:
1. Save and run Python files instead of executing them in the IDLE console.
2. Execute Python programs using the terminal or command prompt.
3. Use PyCharm IDE to write and run Python code.
4. Debug and trace Python programs using breakpoints in PyCharm.

---

## Understanding IDLE vs PyCharm

- **IDLE** is an **interactive console**, suitable for quick testing and small scripts.  
- When working on larger **projects**, it’s better to use an **IDE** (Integrated Development Environment) like **PyCharm**, where you can organize, run, and debug files efficiently.


### 1. Saving Python Files Instead of Running in IDLE Console

To save and run Python code properly:

1. Open **IDLE**.  
2. Write your Python code.  
3. Save the file using `File → Save As`.  
4. Name your file with a `.py` extension, e.g.:
   - `main.py`
   - `muskan.py`
5. You can save the file **anywhere** on your system.

### Example:
```python
print("Hello")
x = 5
y = 6
z = x + y
print(z)
```

Save this file (e.g., `main.py`) before running.

---

## 2. Running the File

You can run Python scripts in multiple ways:

### **a) Using the Run Button in IDLE**
- Save the file first.
- Click **Run → Run Module** or simply press **F5**.

### **b) Using Terminal or Command Prompt**
1. Open the **Terminal** or **Command Prompt**.  
2. Navigate to the folder where your Python file is saved.  
   ```bash
   cd path/to/your/file
   ```
3. Run the file using:
   ```bash
   python main.py
   ```
   or
   ```bash
   python navin.py
   ```

---

## 3. Working with PyCharm

**PyCharm** is a popular Python IDE that provides advanced features like:
- Syntax highlighting  
- Intelligent code completion  
- Integrated terminal  
- Debugging tools  
- Project management  

### Steps to Create and Run Code in PyCharm:
1. Open **PyCharm**.
2. Click on **Create New Project**.
3. Enter a **project name** and click **Create**.
4. Inside the project, right-click → **New → Python File**.
5. Name your file (e.g., `MyCode.py`).
6. Write your Python code:
   ```python
   x = 5
   y = 6
   z = x + y
   print(z)
   ```
7. Save the file.
8. Click on the **Run** button (▶️) at the top or right-click inside the file → **Run 'MyCode'**.

---

## 4. Debugging the Code in PyCharm

Debugging allows you to **analyze your code line by line** and inspect variable values during execution.

### Steps to Debug in PyCharm:
1. Open your Python file.
2. Click to the **left of a line number** to set a **breakpoint** (🔴 red dot appears).
3. Go to the **Run menu** and select **Debug**.
4. Use **Step Over (F8)** to execute code line by line.
5. Observe variable values (`x`, `y`, `z`) in the **Debug window**.

### Example:
```python
x = 5
y = 6
z = x + y
print(z)
```

During debugging, you can:
- Hover over variables to see their values.
- Check the call stack and program flow.
- Fix logical errors effectively.

---

## Summary

| Task | Tool | Description |
|------|------|--------------|
| Run single line of code | IDLE | Quick testing in the interactive shell |
| Save & Run full script | IDLE / Terminal | Execute `.py` files |
| Project development | PyCharm | Create and manage large projects |
| Debugging | PyCharm | Analyze and trace code step by step |

### Key Takeaways
- Use `.py` files for all scripts.
- Use **Terminal** or **PyCharm Run button** to execute.
- Use **Debug mode (F8)** in PyCharm to trace logic.
- IDLE is great for small tasks; PyCharm is better for real projects.

### Additional Resources
- [Download Python](https://www.python.org/downloads/)
- [Download PyCharm](https://www.jetbrains.com/pycharm/download/)

