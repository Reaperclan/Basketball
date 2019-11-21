#game file 
from gamelib import*
#variables 
game = Game(800,800,"Basketball")

bk = Image("shutterstock.jpg",game) 
bk.resizeTo(800,800) 

pewdiepie = Image("pewdiepie.png",game) 
pewdiepie.resizeBy(-50) 
pewdiepie.setSpeed(10,60) 

weeaboo = Image("weeaboo.png",game) 
weeaboo.resizeBy(-40) 
weeaboo.setSpeed(20,20) 

basketball = Image("basketball.png",game) 
basketball.resizeBy(-60) 

#essential game loop 
while not game.over: 
  game.processInput() 
  bk.draw() 
  
  pewdiepie.move(true) 
  weeaboo.move(true) 
  basketball.moveTo(mouse.x,mouse.y) 
  game.update(30) 
  
game.quit()
