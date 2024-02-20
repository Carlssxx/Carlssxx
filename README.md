import tkinter as tk
from tkinter import messagebox

def wish_happy_birthday():
    messagebox.showinfo("Feliz Aniversário!", "Feliz Aniversário, Alinne!")

def button_left_click():
    messagebox.showinfo("Botão Esquerdo", "Você escolheu o botão de dois reais e agora vai ficar querendo!")

def button_right_click():
    messagebox.showinfo("Botão Direito", "Você escolheu o presente misterioso, ele é misterioso!")

root = tk.Tk()
root.title("Feliz Aniversário, Alinne!")

label = tk.Label(root, text="Feliz Aniversário, Alinne!", font=("Helvetica", 16))
label.pack(pady=10)

frame = tk.Frame(root)
frame.pack(pady=10)

button_left = tk.Button(frame, text="Dois Reais", width=12, fg="white", bg="red", command=button_left_click)
button_left.grid(row=0, column=0, padx=10)

label_or = tk.Label(frame, text="ou", font=("Helvetica", 12))
label_or.grid(row=0, column=1)

button_right = tk.Button(frame, text="Presente Misterioso", width=15, fg="white", bg="red", command=button_right_click)
button_right.grid(row=0, column=2, padx=10)

wish_button = tk.Button(root, text="Desejar Feliz Aniversário", command=wish_happy_birthday)
wish_button.pack(pady=10)

root.mainloop()
