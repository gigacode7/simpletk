# SimpleTk documentation

The alias `stk` is recommended for use.

Lastet version: `1.0-beta.0`

**Feedback:**

Mail : gigacode7@outlook.com

Telegram: [Click](https://t.me/wannabestark)
___

## SimpleTk functions
**`root`** is mandatory parameter.

> Main window parameters
```python
stk.window(root, title, width, height)
# title - the title of the window
# width - the width of the window
# height - the height of the window
``` 

> Resizable parameters
```python

stk.sizes(root, width, height) 
# width - resizing by width
# height - resizing by height
width, height = True or False
```

> Button parameters
```python
stk.btn(root, text, command)
# text - the text of the button
# command - the command to execute
```

> Label parameters
```python
stk.lbl(root, text)
# text - the text of the label
```

> Label with setting font parameters
```python
stk.lblf(root, text, font)
# text - the text of the label
# font - the font of the label
```

> Entry parameters
```python
stk.ent(root)
```

> Mainloop parameters
```python
stk.loop(root)
```
> How to get data from entry?

1. Create a new entry
2. Create a button
3. Create a function or use lambda function
4. Done!
```python
import tkinter as tk
import simpletk as stk


root = tk.Tk()

def get():
    text = stk.ent_get()
    stk.lbl(root, text)

stk.ent(root)
stk.btn(root, 'Get data', get)

stk.loop(root)
```
___

## Code examples

> 1. Empty window
```python
import tkinter as tk
import simpletk as stk

root = tk.Tk()

stk.window(root, 'ExampleWindow', 600, 450)
stk.loop(root)
```

> 2. Window with font-label and button
```python
import tkinter as tk
import simpletk as stk

root = tk.Tk()

stk.window(root, 'ExampleWindow', 400, 400)

stk.lblf(root, 'Hello, World!', 'Arial 15 bold')
stk.btn(root, 'Bruh button', lambda: print('bruh'))

stk.loop(root)
```

> 3. Window with fixed geometry
```python
import tkinter as tk
import simpletk as stk

root = tk.Tk()

stk.window(root, 'ExampleWindow', 200, 200)
stk.sizes(root, False, False)

stk.lbl(root, 'idk')

stk.loop(root)
```

___
[Beta release is available!](https://github.com/gigacode7/simpletk/releases)