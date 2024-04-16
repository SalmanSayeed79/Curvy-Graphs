# WaveSim


![Untitled](WaveSim%2090c0eb438045456aa8a83e5e49ff904e/Untitled.png)

## Problem Statement

This was an offline that was given to us for our L1-T1 “CSE 102 | Structured Programming Language Sessional” course. Some of its features were compulsory and we were given a .exe file with all the compulsory features. We had to replicate that in our project.

It was also kept open for additional features and we could build anything extra for bonus marks. I developed a PONG game that follows curvy motion rather than normal linear motion for this task.

![Untitled](WaveSim%2090c0eb438045456aa8a83e5e49ff904e/Untitled%201.png)

## Features

- Creating “n” number of base curves
    - PageUp to add new waves
    - PageDown to remove a wave
- Combining those curves to form a summation curve
    - rightArrow to increase phase by 30deg
    - leftArrow to decrease phase by 30deg
- Changing variables in real-time
- Implementing controls as follows :
    - a for amp decrease
    - A for amp increase
    - f for f increase
    - F for freq decrease
    - q for backscreen
    - x to quit app
- Moving balls along each curve; the balls would hit the wall and change direction
- Changing ball speed
    - + to increase speed
    - - to decrease speed
    - p to pause ball movement
    - r to resume ball movement
- Removing the curves from the screen to show only the balls
    - 0 to hide/show SummationCurve ball
    - 1,2,3,4,5… to hide/show specific ball
- Creating menu for the whole thing

## Stack

iGraphics Framework [Based on OpenGL]

## My solution

I had implemented all the core features and included an extra “Game Mode” where the ball would be treated as a PONG ball and we could control the PONG paddles with different buttons on the keyboard

Extra Features 

- PONG Game
- Ball moves along curve instead of line
- Scoring System
- Multiplayer
    - w,s For player 1
    - UP, DOWN for player 2
    

## Resources

Youtube Demonstration Video

[https://www.youtube.com/watch?v=o-8zyD1PyuI](https://www.youtube.com/watch?v=o-8zyD1PyuI)

Public Github Repository

[GitHub - SalmanSayeed79/Curvy-Graphs: Lab project for 1-1](https://github.com/SalmanSayeed79/Curvy-Graphs/tree/main)

#IGraphics
This is the repository for IGraphics library. IGraphics is a thin wrapper on top of OpenGL. This can be used for simple 2D graphics demonstrations, project work for C programming language course

Command line compiling:
-----------------------
g++ -IOpenGL\include -w -c BallDemo.cpp -o BallDemo.o

Command line linking:
---------------------
g++ -LOpenGL\lib BallDemo.o -o BallDemo.exe -lGlaux -lGLU32 -lglui32 -lglut32 -lOPENGL32 -lgdi32

Command line running:
---------------------
Make sure glut32.dll is present in the same folder
Run BallDemo.exe

Animation Related API:
----------------------
int iSetTimer(int msec, void (*f)(void))
void iPauseTimer(int index)
void iResumeTimer(int index)

Shape drawing:
--------------
void iSetColor(double r, double g, double b)
void iPoint(double x, double y, int size=0)
void iLine(double x1, double y1, double x2, double y2)
void iFilledPolygon(double x[], double y[], int n)
void iPolygon(double x[], double y[], int n)
void iRectangle(double left, double bottom, double dx, double dy)
void iFilledRectangle(double left, double bottom, double dx, double dy)
void iFilledCircle(double x, double y, double r, int slices=100)
void iCircle(double x, double y, double r, int slices=100)
void iEllipse(double x, double y, double a, double b, int slices=100)
void iFilledEllipse(double x, double y, double a, double b, int slices=100)

Text output:
------------
void iText(double x, double y, char *str, void* font=GLUT_BITMAP_8_BY_13)

Rendering:
----------
void iDraw();
void iClear();
void iShowBMP(int x, int y, char filename[])

Initialization:
---------------
void iInitialize(int width=500, int height=500, char *title="iGraphics")

I/O event handling:
-------------------
void iKeyboard(unsigned char);
void iSpecialKeyboard(unsigned char);
void iMouseMove(int, int);
void iMouse(int button, int state, int x, int y);

