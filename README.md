# taptaptap
import tkinter as tk

# создание экземпляра класса Tk(), для отображенния окна приложения
root = tk.Tk()
root.title('Хомяк')
# создаем холст с размерами, цветом
canvas1 = tk.Canvas(root, width=300, height=350, bg='lightsteelblue2', relief='raised')
canvas1.pack()

# создаем текстовую метку
label1 = tk.Label(root, text='Тапай чтобы заработать!', bg='lightsteelblue2')
label1.config(font=('helvetica', 15))
canvas1.create_window(150, 80, window=label1)

tap_counter = 0
def button_tap():
    global tap_counter
    tap_counter += 1
    print(tap_counter)


# создаем кнопку с текстом и размерами
button1 = tk.Button(text='      Тап     ', command=button_tap, bg='green', fg='white',
                    font=('helvetica', 12, 'bold'))
canvas1.create_window(150, 180, window=button1)

# запуск цикла программы
root.mainloop()
