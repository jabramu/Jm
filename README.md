import turtle

import math

port random

import ran

import time

screen = turtle.Screen()

screen.title("Heart Lines")

screen.bgcolor("black")

screen.setup(width=800, height=800)

screen.tracer(0)

t = turtle.Turtle()

t.hideturtle()

t.speed(0)

t.pensize(1)

def heart_x(t_val):

return 16 * math.sin(t_val) ** 3

def heart_y(t_val):

return (13* math.cos(t_val)

- 5* math.cos(2* t_val)

2* math.cos(3 * t_val)

cos(4* t_val))

scale = 15

heart_x(ang) * scale

points = []

for i in range(0, 720):

ang = math.radians(i / 2)

y = heart_y(ang)* scale - 70

points.append((x, y))

colors = ["#ff66b2". "#ff99cc". "#ff4da6", "#ff80bf", "#ff1a8c"]

for_ in range(500):

x, y = random.choice(points)

start_y = random.randint(-10, 10)

t.penup()

t.goto(0, start_y)

t.pendown()

t.color(random.choice(colors))

t.goto(x, y)

screen.update()

t.color("deeppink")

t.pensize(3)

t.penup()

first = True

for x, y in points:

if first

t.goto(x, y)

t.pendown()

first = False

t.goto(x, y)

screen.update() turtle.done()
