---
description: Where you get feedback
---

# Console Window

The console provides helpful feedback such as errors, warnings, and messages.

## Default View

**Note:** This is in a shortened window.

![A clear console](<../../.gitbook/assets/image (55).png>)

![Console showing how each type of console message or "log" appears.](<../../.gitbook/assets/image (60).png>)

Clicking on a message provides more information:

![Console with detailed information](<../../.gitbook/assets/image (74).png>)

### **Errors**

**How to read the error above:**

| What                                   | Seen in Console Message            |
| -------------------------------------- | ---------------------------------- |
| Printed message**:**                   | This is an example of an error.    |
| What code printed the error:           | UnityEngine.Debug.LogError(Object) |
| Name of the script catching the error: | SampleMessage.cs                   |
| Function name within the script:       | Update()                           |
| File path of the script:               | Assets/Scripts/SampleMessage.cs    |
| Line with error or error catch:        | 18                                 |

## Options

![](<../../.gitbook/assets/image (56).png>)

**Clear **- Clears messages, warnings, and errors.

**Collapse** - Similar messages can be collapsed, resulting in one full message and the number of instances to the right. When not collapsed, the full message appears repeatedly.

![Collapse is turned on](<../../.gitbook/assets/image (57).png>)

![Collapse is turned off](<../../.gitbook/assets/image (58).png>)

**Clear on Play** - When on, past messages are cleared when Play is clicked

**Error Pause** - When selected, the game will pause when it encounters an error. This helps for errors that aren't big enough to "break" the visuals of the game and might get buried in Console messages.

**Editor (Dropdown) **- Provides more options about what messages are displayed.

**Search **- Results will appear and the term will be highlighted in blue. Click the x on the right side of the bar to clear the search.

**Count **- Number of messages, warnings, and errors. You can toggle these by clicking on the type you want to hide or show.** **

![](<../../.gitbook/assets/image (59).png>)
