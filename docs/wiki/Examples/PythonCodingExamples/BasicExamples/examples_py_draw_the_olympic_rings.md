## Project Introduction
In this project, we will be creating the Olympic Rings, an iconic symbol consisting of 5 different colored rings. The draw_circle function from the GUI class will be utilized to showcase how to create these graphical elements and combine them to form the image.  
  
![1720429408029.jpg](img/10. Draw the Olympic Rings/1720429431689-e8440db3-40bc-46c4-85f4-6fe0df8ecc96.jpg){width=300, style="display:block;margin: 0 auto"}  

## Hardware Required

- [UNIHIKER](https://www.dfrobot.com/product-2691.html)
## Code 
In this interactive example, users will be able to draw the five Olympic Rings using the draw_circle function from the Unihiker GUI library. The process begins with a single blue ring and with every subsequent user click, an additional ring will appear, completing the formation. A prompt in the terminal, "Please click to draw a new circle," will instruct the user to continue the sequence.
The first ring, a blue circle with a radius of 23 and line width of 5 at coordinates (65, 125), will be displayed. As shown in line 24 of the following code, the onclick attribute is assigned a callback function, ring_click1, defined in line 3. This function will keep track of the number of rings clicked and generate the next ring in its designated position.
As the user continues to interact with the program, subsequent rings will be drawn in response to each click. The black ring will appear at (120, 125), followed by the red ring at (175, 125), the yellow ring at (90, 150), and finally, the green ring at (150, 150).
A loop with time.sleep(1) is used to keep the program running and allow users to view and interact with the evolving drawing. This also ensures that the program does not end too quickly.
```python
from unihiker import GUI
# button callback function
def ring_click1():
    global step
    
    if (step == 1):
        circle2=gui.draw_circle(x=120, y=125, r=23, width=5,color="black",onclick=ring_click1)
        step = (step + 1)
        print("Please click to draw a new circle")
    elif (step == 2):
        circle3=gui.draw_circle(x=175, y=125, r=23, width=5,color="red",onclick=ring_click1)
        step = (step + 1)
        print("Please click to draw a new circle")
    elif (step == 3):
        circle4=gui.draw_circle(x=90, y=150, r=23, width=5,color="yellow",onclick=ring_click1)
        step = (step + 1)
        print("Please click to draw a new circle")
    elif (step == 4):
        circle5=gui.draw_circle(x=150, y=150, r=23, width=5,color="green",onclick=ring_click1)
        step = (step + 1)
        print("Please click to draw a new circle")
        
gui = GUI()
circle1=gui.draw_circle(x=65, y=125, r=23, width=5,color="blue",onclick=ring_click1)
# Draw the first circle, set
print("Please click to draw a new circle")
step = 1

while True:
    pass

```
## Demo Effect
![101010.gif](img/10. Draw the Olympic Rings/1720429334052-dba5c37d-eaef-4d2c-a32e-0d05d8d01495.gif){width=300, style="display:block;margin: 0 auto"}  
![image.png](img/10. Draw the Olympic Rings/1704861477637-34b9369a-91c7-4be9-ac42-47f3c897e1f1.png){width=500, style="display:block;margin: 0 auto"}
