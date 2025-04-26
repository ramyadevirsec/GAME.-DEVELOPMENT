# EX 2 : Bresenham‘s Line Drawing Algorithm

**AIM :**

 To  implement the Bresenham’s  algorithm for line using a c coding.

**ALGORITHM :**

   Step 1 : Start.
   
   Step 2 : Initialize the graphics header files and functions.

   Step 3 : Declare the required variables and functions.

   Step 4 : Get the four points for drawing a line namely x1,x2,y1,y2.

   Step 5 : Draw the line using the algorithm.

   Step  6 : Display the output.

   Step 7 : stop.

## NAME:SATHISH.B
## REG NO:212224040299

**Program :**
```#include "stdio.h" 
#include "conio.h" 
#include "math.h" 
#include "graphics.h" 
main() 
{ 
  int gd=DETECT,gm; 
  int xa,xb,ya,yb; 
  int dx,dy,x,y,xend,p; 
  initgraph(&gd,&gm,"c:\\tc\\bgi"); 
  printf("Enter The Two Left Endpoints(xa,ya):\n"); 
  scanf("%d%d",&xa,&ya); 
  printf("Enter The Two Right Endpoints(xb,yb):\n"); 
  scanf("%d%d",&xb,&yb); 
  dx=abs(xa-xb); 
  dy=abs(ya-yb); 
  p=2*dy-dx; 
  if(xa>xb) 
  { 
   x=xb; 
   y=yb; 
   xend=xa; 
  } 
 else 
{  
  x=xa; 
   y=ya; 
   xend=xb; 
} 
      putpixel(x,y,6); 
     while(x<xend) 
      { 
      x=x+1; 
      if(p<0) 
      { 
      p=p+2*dy; 
      } 
      else   
      { 
      y=y+1; 
      p=p+2*(dy-dx);   
      } 
      putpixel(x,y,6); 
      } 
   getch(); 
   return(0); 
}
```

**Output :**
![Screenshot (12)](https://github.com/user-attachments/assets/fa205f12-8cc0-470c-857b-4248b485781e)


**Result :**

The Bresenham’s line drawing algorithm was successfully implemented in C. The line was accurately drawn between the given points using efficient pixel plotting.
