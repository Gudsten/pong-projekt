#Pong med en twist

import turtle
import time

# Set up the screen
win = turtle.Screen()
win.title("Pong Game")
win.bgcolor("black")
win.setup(width=800, height=600)
win.tracer(0)

score_a = 0
score_b = 0

# Paddle A
paddle_a = turtle.Turtle()
paddle_a.speed(0)
paddle_a.shape("square")
paddle_a.color("white")
paddle_a.shapesize(stretch_wid=6, stretch_len=1)
paddle_a.penup()
paddle_a.goto(-350, 0)

# Paddle B
paddle_b = turtle.Turtle()
paddle_b.speed(0)
paddle_b.shape("square")
paddle_b.color("white")
paddle_b.shapesize(stretch_wid=6, stretch_len=1)
paddle_b.penup()
paddle_b.goto(350, 0)
 # Obstacle and ball collision
    if obstacle_left.isvisible() and (-195 < ball.xcor() < -155 and obstacle_left.ycor() - 50 < ball.ycor() < obstacle_left.ycor() + 50):
        if abs(ball.xcor() + 175) > abs(ball.ycor()):
            ball.dx *= -1
        else:
            ball.dy *= -1

    if obstacle_right.isvisible() and (155 < ball.xcor() < 195 and obstacle_right.ycor() - 50 < ball.ycor() < obstacle_right.ycor() + 50):
        if abs(ball.xcor() - 175) > abs(ball.ycor()):
            ball.dx *= -1
        else:
            ball.dy *= -1
