# Python Debugging Tips

If (or when) your code throws an error, you'll see a large stacktrace in the terminal. Here's how you can find the bug.

Go all the way to the bottom of the stacktrace to find the line that the error occured on. Is this a line of code you wrote? If so, you can Google the error message to figure out what's wrong.

If it's code you didn't write, you _most likely_ called a function we provided you with the incorrect parameters (keep in mind python is interpreted and not strongly typed). To find the bug, move up the stacktrace until you find code that you wrote.

Once you find the errors, you can use a debugger to help figure out why the errors occur. Please refer to the other guide for information on how to use **PyCharm** and its built-in debugger.