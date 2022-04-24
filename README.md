# ping-pong
algoritmika work
from py import *
 
WIDTH = 900
HEIGHT = 300
 
PAD_W = 10
PAD_H = 100
 
BALL_RADIUS = 30
 
root = Tk()
root.title("PythonicWay Pong")
 
c = Canvas(root, width=WIDTH, height=HEIGHT, background="#003300")
c.pack()
 
c.create_line(PAD_W, 0, PAD_W, HEIGHT, fill="white")

c.create_line(WIDTH-PAD_W, 0, WIDTH-PAD_W, HEIGHT, fill="white")

c.create_line(WIDTH/2, 0, WIDTH/2, HEIGHT, fill="white")
 
BALL = c.create_oval(WIDTH/2-BALL_RADIUS/2,
                     HEIGHT/2-BALL_RADIUS/2,
                     WIDTH/2+BALL_RADIUS/2,
                     HEIGHT/2+BALL_RADIUS/2, fill="white")
 
LEFT_PAD = c.create_line(PAD_W/2, 0, PAD_W/2, PAD_H, width=PAD_W, fill="yellow")
 
RIGHT_PAD = c.create_line(WIDTH-PAD_W/2, 0, WIDTH-PAD_W/2, 
                          PAD_H, width=PAD_W, fill="yellow")
 

root.mainloop()
