from tkinter import*
import random
def next_turn():
    pass
def chech_winner():
    pass
def empty_spaces():
    pass
def new_game():
    pass
window = Tk()
window.title("Tic-Tac-Toe")
players = ["X","O"]
starter_player = random.choice(players)
buttons = [[0, 0, 0],
           [0, 0, 0],
           [0, 0, 0]]
label = Label(text=starter_player + "turn", font=('consolas', 40))
label.pack(side="top")
reset_button = Button(text="restart", font="consolas", command=new_game)
reset_button.pack(side="top")
window.mainloop()
