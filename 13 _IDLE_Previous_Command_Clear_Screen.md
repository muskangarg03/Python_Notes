# IDLE Previous Command & Clear Screen  

In this lecture, we learn how to configure **Python IDLE** to navigate through previous and next commands, similar to how we use the command prompt (CMD).  


## Why Configure IDLE History?  
When working in Python IDLE, you may often repeat commands or want to quickly re-run previous ones.  
- In **CMD**, we use the **Up** and **Down** arrow keys to access history (`ipconfig`, `mkdir`, `help`, etc.).  
- By default, IDLE does not provide this feature.  
- But we can **configure IDLE** to use arrow keys for history navigation.  


---


## Steps to Configure IDLE History  
Follow these steps to enable **previous/next command navigation** in IDLE:  

1. Open **Options** from the IDLE menu bar.  
2. Select **Configure IDLE**.  
3. Go to the **Keys** tab.  
4. Scroll down and find:  
   - `history-previous`  
   - `history-next`  
5. Click **Get New Keys for Selection**.  
6. Assign:  
   - **Up Arrow Key** → `history-previous`  
   - **Down Arrow Key** → `history-next`  
7. Click **OK** and close the IDLE configuration window.  

Now you can use the **Up** and **Down** arrow keys in IDLE just like in CMD.  


### Example Usage  

```python
>>> x = 2 + 4 + 9
>>> x = 2 + 4 + 9   # (Press Up Arrow to repeat previous command)
```

- Press **Up Arrow** → Brings previous command.
- Press **Down Arrow** → Moves forward in history.


---


## Clear Screen in IDLE
Unlike CMD or terminal, Python IDLE does not provide an option to clear the screen or history.
- You can close and reopen IDLE to start fresh.
- Alternatively, you can use an IDE (like PyCharm, VS Code, Jupyter Notebook), which provides clear screen options.


---


## Summary
- IDLE can be configured to navigate command history using Up/Down Arrow keys.
- This saves time when reusing previous commands.
- Clear Screen is not supported in IDLE, only restarting IDLE resets the session.
