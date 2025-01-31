## Day 4 -  Pre-layout timing analysis and importance of good clock tree

### <br> Timing modelling using delay tables
 
As of now, we have done till placement in the flow and extracted a spice file given a .magic file. Now if we see into the amgic layout, it has many kinds of information, but we donot need that file for routing purpose. We need the info inside that layout. And this is where the .lef file comes in picture. This lef file contains all the info. So our first task will be the extraction of lef file. But beforehand we should know some guidelines---

1st- Always put input and output ports on the intersection of the vertical and the horrizontal tracks. 

2nd - The width of the standard cell must be in the odd multiples of the track pitch and the height in the odd multiples of the vertical track pitch.

