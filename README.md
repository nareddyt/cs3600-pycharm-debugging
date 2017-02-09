# Debugging with PyCharm

We (Georgia Tech's CS 3600 TAs) made this tutorial to introduce **PyCharm** to students taking the course. Two main reasons for using PyCharm over a text editor:

* Dynamic error checking and warning messages
* A built-in debugger

We will go over the debugger towards the end of the tutorial. If you already have PyCharm set up and working, you can skip right to that part.

This tutorial assumes students used **IntelliJ IDEA** in CS 1332. Students who have not used IntelliJ should be able to follow along, but it might take time to get used to the GUI and keyboard shortcuts.

## Introduction to JetBrains Products

**JetBrains** is a company that creates development tools for programmers. A full list of IDEs and tools can be found [here](https://www.jetbrains.com/products.html?fromMenu). For our course, we will be using their Python IDE called **PyCharm**.

You can download PyCharm [here](https://www.jetbrains.com/pycharm/download/#section=windows). There are two different versions:

* **Community**: Free for everyone to use and has all the features needed for our course. _We recommend this version._
* **Professional**: Developed for corporations, has lots of enterprise-level features. Requires a license.

### Get a Student Account (Optional)

JetBrains offers all their professional tools for free to students! You can create a student account [here](https://www.jetbrains.com/student/). We won't go into much more detail on this, as this is not a required step.

## Initial Setup

After downloading and installing PyCharm, run the application. You will have to choose a few options for the initial setup, but this should only take a few seconds. 

We recommend that you stick to all the default settings. However, feel free to change the theme: `Dracula` looks similar to **Atom** and **Sublime Text**.

## Opening Projects in PyCharm

This is pretty self explanatory. Make sure the project folder is downloaded and you know where it is.

Click on the `Open` button in the welcome screen, select the project folder in the navigation view, and click `Ok`.

Note that when you open the project, PyCharm will create a hidden directory called `.idea` in the project folder. You shouldn't worry about this, but don't delete it!

## Setting the Python Environment

Usually, PyCharm is able to find your default Python installation path. However, if your laptop is set up incorrectly, you will need to explicitly specify the path. Follow these steps to check:

1. `File` -> `Settings`
2. Select `Project` -> `Project Interpreter` on the left of the settings menu
3. Make sure `Python 2.7.*` is selected in the dropdown menu (the * can be any number)

If you see python in the dropdown menu, you can skip to the next section. Otherwise:

1. Select `Show All` in the dropdown menu.
2. Click on the green plus button.
3. Add the directory to `python.exe`. Depending on your operating system, you might have to Google where you can find the executable on your computer. For Windows users, it's in the Python2.7 folder either in `C:/Program Files` or `C:/Program Files (x86)`.

## Running the Autograder

Instead of using the terminal to run the autograder, we will create a `Run Configuration`. With this, you will be able to re-run the command (and later use the debugger) without having to re-type the entire command.

### Running `python autograder.py`

We wish to run the autograder with no extra parameters (no `-q q1`). Here is how we can do that:

1. Open `autograder.py` by double-clicking on it on the `Project Menu` toward the left
2. Scroll down until you see:

```python
if __name__ == "__main__":
```
Click the green run button to left. This will run the autograder, which is the equivalent of typing in `python autograder.py` into the terminal.

Notice how this has created a `Run Configuration` on the top left. Any files you run will show up in this dropdown menu. To re-run any of these, you can select it in the menu and press on the green arrow to the right.
