# HiOS
A weird virtual OS written in Python

## Source
```python
from tkinter import *

def shut():
    os.destroy()      

def light():
    global themeblack
    os.configure(bg="#F0F8FF")
    text.configure(bg="aqua", fg="black")
    shutdown.configure(bg="aqua", fg="black")
    theme.pack_forget()
    themeblack = Button(os, text = "Theme", font=("classic console neue", 50), width=10,bg="aqua", fg="black", border=0, command=dark)
    themeblack.pack(pady=5)

def dark():
    os.configure(bg="black")
    text.configure(bg="black", fg="aqua")
    shutdown.configure(bg="black", fg="aqua")
    themeblack.pack_forget()
    theme = Button(os, text = "Theme", font=("classic console neue", 50), width=10,bg="#101010", fg="aqua", border=0, command=dark)
    theme.pack(pady=5)


os = Tk()
os.state("zoomed")
os.wm_attributes("-toolwindow", True)
os.configure(bg="black")

text = Label(os, text="HiOS", font=("classic console neue", 150), bg="black", fg="aqua")
text.pack(pady=70)

shutdown = Button(os, text = "Shutdown", font=("classic console neue", 50), width=10,bg="#101010", fg="aqua", border=0, command=shut)
shutdown.pack(pady=5)

theme = Button(os, text = "Theme", font=("classic console neue", 50), width=10,bg="#101010", fg="aqua", border=0, command=light)
theme.pack(pady=5)

os.mainloop()```
