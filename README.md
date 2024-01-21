from tkinter import*
import random
def next_turn(row, column):
    global player
    if buttons[row][column]['text'] == "" and check_winner() is False:
        if player == players[0]:
            buttons[row][column]['text'] = player
            if check_winner() is False:
                player = players[1]
                label.config(text=(players[1]+" turn"))
            elif check_winner() is True:
                label.config(text=(players[0]+" wins"))
            elif check_winner() == "Tie":
                label.config(text="Tie!")
        else:
            buttons[row][column]['text'] = player
            if check_winner() is False:
                player = players[0]
                label.config(text=(players[0]+" turn"))
            elif check_winner() is True:
                label.config(text=(players[1]+" wins"))
            elif check_winner() == "Tie":
                label.config(text="Tie!")
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
