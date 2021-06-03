import random
from tkinter import *
root=Tk()
root.geometry("700x400")
root.title("Roll dice")

label=Label(root,font=("times",200),foreground="green")
def roll_dice():
    dice=['\u2680','\u2681','\u2682','\u2683','\u2684','\u2685']
    print(f'{random.choice(dice)} {random.choice(dice)}')
    label.configure(text=f'{random.choice(dice)} {random.choice(dice)}')
    label.pack()

Button=Button(root,text='lets roll....',command=roll_dice)
Button.pack()

root.mainloop()
