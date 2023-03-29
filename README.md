# SimpleTk by Giga Code

![pypi version](https://img.shields.io/pypi/v/simpletk "pypi") 

#### This module will help in writing Tkinter programs. It is currently under development, but a limited alpha pre-release is now available. The prerelease corrections will be released. New features will be added, but published less frequently.
___
### How to install SimpleTk
```
pip install simpletk
```
___
### Examples of code using SimpleTk
The first thing you should do is import the libraries, it is recommended to assign an alias.
```python
import tkinter as tk
import simpletk as stk
```

Now let's talk about how to write code using the module. 

In alpha version 0.1.0 only 4 functions are available, they are specified in the [release description](https://github.com/gigacode7/simpletk/releases)

Let's create a window with a label
```python
import tkinter as tk
import simpletk as stk

root = tk.Tk()
stk.window(root, 'Hello World')
```
Enter the parameters.  Nothing will work without root, this is a mandatory parameter. The second parameter is the window title.

If we run this code, nothing will happen because we haven't started the loop. So let's do it!
```python
import tkinter as tk
import simpletk as stk

root = tk.Tk()
stk.window(root, 'Hello World')
stk.loop(root)
```

Now the code is working, but so far it's kind of empty. Let's add some text
```python
import tkinter as tk
import simpletk as stk

root = tk.Tk()
stk.window(root, 'Hello World')
stk.lbl(root, 'Simple label!')
stk.loop(root)
```

It's almost the same as with the window, we'll add a button right away
```python
import tkinter as tk
import simpletk as stk

root = tk.Tk()
stk.window(root, 'Hello World')
stk.lbl(root, 'Simple label!')
stk.btn(root, 'Simple button!', command=lambda: print('This is work!'))
stk.loop(root)
```
The command parameter is already being added here, for which we have created a lambda function.
___
And now let's compare 2 codes: without using SimpleTk, and with using SimpleTk

>Without SimpleTk:
```python
import tkinter as tk

root = tk.Tk()
root.title('Hello World')
root.geometry('450x450')

label = tk.Label(root, text='Simple Label!')
label.pack()

button = tk.Button(root, text='Simple Button!', command=lambda: print('This is work!))
button.pack()

root.mainloop()
```

>With SimpleTK:
```python
# v0.1.0-alpha
import tkinter as tk
import simpletk as stk

root = tk.Tk()
stk.window(root, 'Hello World')
stk.lbl(root, 'Simple label!')
stk.btn(root, 'Simple button!', command=lambda: print('This is work!'))
stk.loop(root)
```
I think the difference is visible
___
### See you in the next releases!
