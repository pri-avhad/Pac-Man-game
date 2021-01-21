# Pac-Man-game

```
+XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX+  
|..........             P             |   20
|         ......E                     |
|XX   XXXXX       XXXXXXXX   XXXXXXXXX|
|     |           XXXXXXXX   XXXXXXXXX|
| |   |XXX|  |    XXX        |        |
| |   |XXX|  |    XXX    |   |        |
| |   |XXX|  |    XXX    |   |        |
| |          |XX         |   |        |
| |XXXXX     |XX                      |
|            |XX   XXXXXXX            |
|XXXXXXXXX                   XXXXXXXXX|
|XXXXXXXXX    XXXXXXXXXXXX            |
|        |    |          |   |XXXXXXXX|
|                                     |
|                                     |
|                                     |
+XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX+
```

Implemented a pac-man game using a simple path finder algorithm. The game includes three difficulty levels namely hard, medium and easy. 

This project is aimed at designing an intelligent pac-man agent that is able to find optimal paths through its maze world considering both reaching particular locations (e.g., finding all the corners) and eating the pac-man in as few steps as possible. It is implemented using a graph search algorithm known as Breadth First Search to find the shortest path between pac-man and eater.


Working:
The  map for the Pac-man game has been predefined in the code.
* Showfield() : This function is used to print the map on the console.
* set_coor() : This function is used to get the control over the console. It declares your cursor position as a COORD structure with two parameters X, and Y (where X represents the column and Y the line). SetConsoleCursorPosition( ) in the function that actually gives you the full control on the cursor position. It takes two arguments: the first is the variable which holds control on the console window and the second is the coordinate x,y pair.
* AddArray() : This function checks the presence of an empty space or absence of a wall and adds an instance of the structure walk in the BFS Array to determine the optimal path eventually. 
* FindPath() : This function  is used to find the shortest path between Pac-Man and the eater using breadth-first search algorithm in graph. BFS does correctly find the shortest path between nodes in unweighted graphs. In an unweighted graph, the length of a path is simply the number of edges from the source to the destination.
The pac-man board can be thought of as an unweighted graph: Each square of the board (that is not a wall) is a node, and has edges to its direct neighbors.
When an eater searches for the shortest path to pac-man, it starts a BFS search on this graph from the square it sits on. Once the search finds pac-man, we can backtrack our way back to find the shortest path. We will obtain a series of moves (e.g. North -> West -> South ...), and the eater will need to follow this path to get to the current location of pac-man.
However, if pac-man is also moving at the same time as the eater, we need to re-run BFS after every move to find the shortest path to the new position.
* main() : This function consists of a menu driven code and continues till the user wishes to play the game. The GetAsyncKeyState simply tells you whether a given key is pressed down at the instant you call the function. GetAsyncKeyState() is normally used as a part of a game loop, for games that update themselves constantly. The score is calculated according to the moves made by the pac-man and displayed after the coordinates of the eater and the pac-man become equal.

For report refer: https://docs.google.com/document/d/1CmEfczsTp9mnkPKoWUTdHN8prQS9lCRpRtQDOZHipHg/edit?usp=sharing

To understand how the shortest path is found you could watch: https://www.youtube.com/watch?v=KiCBXu4P-2Y
