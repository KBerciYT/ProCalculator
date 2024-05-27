from gc import callbacks
import tkinter
from tkinter import messagebox
import customtkinter


def Addition():

    if str.isdigit(firstNumber.get()) & str.isdigit(secondNumber.get()):
        addend = float(firstNumber.get()) + float(secondNumber.get())
        Answer.configure(text=addend)
    
    else:
        Answer.configure(text="Something went wrong...")
        

def Substraction():
        
    if str.isdigit(firstNumber.get()) & str.isdigit(secondNumber.get()):
        subsend = float(firstNumber.get()) - float(secondNumber.get())

        if subsend == 0:
            Answer.configure(text="0")  

        else:
            Answer.configure(text=subsend)

    else:
            Answer.configure(text="Something went wrong...")

    

def Multiplication():

    if str.isdigit(firstNumber.get()) & str.isdigit(secondNumber.get()):
        multiend = float(firstNumber.get()) * float(secondNumber.get())
        Answer.configure(text=multiend)
        
    else:
        Answer.configure(text="Something went wrong...")

def Division():
    
    if str.isdigit(firstNumber.get()) & str.isdigit(secondNumber.get()):
        diviend = float(firstNumber.get()) / float(secondNumber.get())
        Answer.configure(text=diviend)
        
    else:
        Answer.configure(text="Something went wrong...")


customtkinter.set_default_color_theme("blue")

window = tkinter.Tk()
window.title("ProCalculator by KBerci")
window.geometry("800x600") 
window.tk.call("tk", "scaling", 2.0)

lbl = tkinter.Label(window,text="Your first number:")
lbl.grid(column=0, row=0)

number1 = tkinter.StringVar
firstNumber = tkinter.Spinbox(window)
firstNumber.grid(column=0, row=2,pady=20, padx= 10)


lbl2 = tkinter.Label(window,text="Your second number:")
lbl2.grid(column=1, row=0,pady=20, padx= 10)

secondNumber = tkinter.Spinbox(window)
secondNumber.grid(column=1, row=2)

lbl3 = tkinter.Label(window,text="Select the calculation type:")
lbl3.grid(column=1, row=3,pady=20, padx= 10)

lbl4 = tkinter.Label(window,text="ProCalculator made by KBerci")
lbl4.grid(column=1, row=7,pady=20, padx= 10)

addition = tkinter.Button(window, text="Addition (+)", command=Addition)
addition.grid(column=0, row=4,pady=20, padx= 10)

substraction = tkinter.Button(window, text="Substraction (-)", command=Substraction)
substraction.grid(column=1, row=4,pady=20, padx= 10)

multiplication = tkinter.Button(window, text="Multiplication (*)", command=Multiplication)
multiplication.grid(column=2, row=4,pady=20, padx= 10)

division = tkinter.Button(window, text="Division (/)", command=Division)
division.grid(column=1, row=5,pady=20, padx= 10)

Answer = tkinter.Label(window, text="Your answer will show up here!")
Answer.grid(column= 1, row= 6, pady=40, padx= 10)

window.mainloop()

