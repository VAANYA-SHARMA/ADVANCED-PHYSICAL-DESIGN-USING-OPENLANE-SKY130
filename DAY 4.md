# Day 4 -  Pre-layout timing analysis and importance of good clock tree

## <br> Timing modelling using delay tables
### <br> LAB STEPS TO CONVERT GRID INFO TO TRACK INFO...
 
As of now, we have done till placement in the flow and extracted a spice file given a .magic file. Now if we see into the amgic layout, it has many kinds of information, but we donot need that file for routing purpose. We need the info inside that layout. And this is where the .lef file comes in picture. This lef file contains all the info. So our first task will be the extraction of lef file. But beforehand we should know some guidelines---

1st- Always put input and output ports on the intersection of the vertical and the horrizontal tracks. 

2nd - The width of the standard cell must be in the odd multiples of the track pitch and the height in the odd multiples of the vertical track pitch.

What a track actually is??

![image](https://github.com/user-attachments/assets/2f3b68bb-c410-486a-bb51-457788411905)

Tracks are basically the instructions telling where the routing should go... they have these for every metal layer..

Now out guidelines mentioned initially, one stated that "Always put input and output ports on the intersection of the vertical and the horrizontal tracks."

<BR> ![image](https://github.com/user-attachments/assets/758a39d6-e0ae-4233-8bb4-c95d2f0f21dc)

### <br> LAB STEPS TO CONVERT MAGIC LAYOUT TO STD CELL LEF

2nd guideline stated "The width of the standard cell must be in the odd multiples of the track pitch and the height in the odd multiples of the vertical track pitch". 

<BR> ![image](https://github.com/user-attachments/assets/758a39d6-e0ae-4233-8bb4-c95d2f0f21dc)


We can even save a cell to give a sense of belongingness

<br> ![image](https://github.com/user-attachments/assets/65acc1f7-f831-470a-9aaa-c7dd56223c78)
<br> ?![image](https://github.com/user-attachments/assets/84e17e7f-e9cd-4856-871e-7a82c14c8b75)



Now we create a lef file:

![image](https://github.com/user-attachments/assets/d868d281-c1b2-4b4b-b963-8fcd56bef341)

![image](https://github.com/user-attachments/assets/729dcd4b-ef49-4082-82f0-266373c6c352)
<br> The created lef file can be seen (the last file) 

The changes we make in a magic file is seen in this file

![image](https://github.com/user-attachments/assets/cf4d79dd-0538-4135-bc38-0f3313005111)





















