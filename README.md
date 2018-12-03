# Canvas-Drawing
This is a simple console based Java application in which users can create a canvas and draw line,rectangle and color inside it.
# Description
This program is a simple console version of a drawing program. 
At this time, the functionality of the program is quire limited but this might change in the future. 
In a nutshell, the program will work as follows:
 1. Create a new canvas
 2. Start drawing on the canvas by issuing various commands
 3. Quit
# Dependencies
- Programming Language: Java 8
- Build Tool : Maven 
# Commands availble

```
Command 		Description
C w h           Should create a new canvas of width w and height h.
L x1 y1 x2 y2   Should create a new line from (x1,y1) to (x2,y2). Currently only
                horizontal or vertical lines are supported. Horizontal and vertical lines
                will be drawn using the 'x' character.
R x1 y1 x2 y2   Should create a new rectangle, whose upper left corner is (x1,y1) and
                lower right corner is (x2,y2). Horizontal and vertical lines will be drawn
                using the 'x' character.
B x y c         Should fill the entire area connected to (x,y) with "colour" c. The
                behaviour of this is the same as that of the "bucket fill" tool in paint
                programs.
Q               Should quit the program.
``` 

# Sample I/O
```
Below is a sample run of the program. User input is prefixed with enter command:
enter command: C 20 4
----------------------
|                    |
|                    |
|                    |
|                    |
----------------------

enter command: L 1 2 6 2
----------------------
|                    |
|xxxxxx              |
|                    |
|                    |
----------------------

enter command: L 6 3 6 4
----------------------
|                    |
|xxxxxx              |
|     x              |
|     x              |
----------------------

enter command: R 14 1 18 3
----------------------
|             xxxxx  |
|xxxxxx       x   x  |
|     x       xxxxx  |
|     x              |
----------------------

enter command: B 10 3 o
----------------------
|oooooooooooooxxxxxoo|
|xxxxxxooooooox   xoo|
|     xoooooooxxxxxoo|
|     xoooooooooooooo|
----------------------
```
# Assumptions
- Commands are not case sensitive
- Drawing diagnol line is not supported
- When a command receives fewer arguments than expected, it will throw an exception but if it receives more than specifed arguments, it will just ignore the extra arguments.
# To Execute
- From prebuilt JAR: java -jar Canvas-Drawing-0.0.1-SNAPSHOT.jar
- Run program: mvn exec:java
