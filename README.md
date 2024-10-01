# ovalimport turtle

# Set up the screen
screen = turtle.Screen()
screen.bgcolor("white")

# Create a turtle object
pen = turtle.Turtle()
pen.shape("turtle")
pen.speed(1)

# Function to draw an oval
def draw_oval(radius1, radius2):
    pen.up()  # Pen up to move without drawing
    pen.goto(0, -radius2)  # Start position at the bottom of the oval
    pen.down()  # Pen down to start drawing
    pen.setheading(45)  # Set the initial direction

    for _ in range(2):
        pen.circle(radius1, 90)  # Draw the longer side
        pen.circle(radius2, 90)  # Draw the shorter side

# Call the function to draw an oval
draw_oval(100, 50)

# Hide the turtle after drawing
pen.hideturtle()

# Keep the window open until clicked
screen.exitonclick()
