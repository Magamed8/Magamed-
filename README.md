# print("Welcome to Tic Tac Toe")
print("----------------------")

possibleNumbers = [1,2,3,4,5,6,7,8,9]
gameBoard = [[1,2,3],[4,5,6],[7,8,9]]
rows = 3
cols = 3

def printGameBoard():
  for x in range (rows):
    print("\n+---+---+---+")
    print("|", end="")
for x in range(cols):
      print("", gameBoard[x], end=" |")
      print("\n+---+---+---+")
print(printGameBoard())
