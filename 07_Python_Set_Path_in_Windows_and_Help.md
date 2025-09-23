# Python Setup and Help Function

This lecture guides how to **set up Python on Windows**, configure its **system path**, and use the **help() function** for documentation.


## 1. Verifying Python Installation

You can check if Python is installed and view its version using the **Command Prompt (CMD)**:

```cmd
python            # Opens Python interpreter if installed
python --version  # Displays installed Python version
```

---


## 2. Python Installation Path

Python is installed in:

- `C:\Python27` or `C:\Python34` (older versions)  
- Or in the user directory:  
  `C:\Users\<username>\AppData\Local\Programs\Python\Python34\python.exe`

> Copy the full path to `python.exe` for setting the system environment variable.

---


## 3. Setting Python Path in Windows

### a) Temporary Path Setup (CMD session only)

1. Open **Command Prompt**.  
2. Set the path using the command:

```cmd
set path=C:\Users\<username>\AppData\Local\Programs\Python\Python34
```

3. Verify Python:

```cmd
python
>>> 2 + 3
5
>>> print("Hello World")
Hello World
```

> This path will only remain active for the current CMD session.

### b) Permanent Path Setup (Environment Variable)

1. Right-click **My Computer** → select **Properties**.  
2. Click **Advanced System Settings**.  
3. Click **Environment Variables**.  
4. Under **System Variables**, find and select `Path` → click **Edit** → **New**.  
5. Paste the Python executable path:

```
C:\Users\<username>\AppData\Local\Programs\Python\Python34
```

6. Click **OK** on all dialogs.  
7. Restart **CMD** (or your PC) and type:

```cmd
python
```

If Python launches successfully, the setup is complete.

---


## 4. Using the `help()` Function in Python

Python provides a built-in help system to access documentation for modules, functions, keywords, and topics.

### Accessing Help

```python
help()           # Opens interactive help system
help> topics      # Displays general Python topics
help> modules     # Lists available modules
help> keywords    # Shows all Python keywords
help> quit        # Exit the help system

```


### Help on Specific Topics

```python
help('list')       # Displays detailed information about lists
help('modules')    # Shows installed modules
```

> The `help()` function is essential for exploring Python’s built-in features and documentation interactively.

---

## ✅ Summary

- Verify Python installation using `python` or `python --version` in CMD.  
- **Temporary path** → set using `set path=<python_path>` in CMD.  
- **Permanent path** → add Python executable to **System Environment Variables**.  
- Use `help()` to explore Python topics, modules, keywords, and functions interactively.  
- Proper path setup ensures Python works seamlessly from any CMD session.
