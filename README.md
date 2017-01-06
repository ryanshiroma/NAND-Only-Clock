# Clock using only NAND Gates!
*WORK IN PROGRESS*

I got inspiration for this project from [Ahmed Mohamed](https://en.wikipedia.org/wiki/Ahmed_Mohamed_clock_incident) and his "bomb"-ass clock.

The idea for this project is to create a clock using only 2-input NAND gates to learn about circuit minimimzation and PCB design. 
Here I will explain how to design a clock from the transistor level all the way to PCB fabrication.


NAND gates are [functionally complete](https://en.wikipedia.org/wiki/Functional_completeness) which means any logic equation using any combination of logical operators can be re-expressed using only NAND operators. *explain this later*
<img src="https://upload.wikimedia.org/wikipedia/commons/c/cc/Logic-gate-nand-us.png" width=200>

A clock display output(ex. "2:30PM") can be simplified into one of these logical equations which can then converted into a series of NAND gates.

This circuit of NAND gates then gets turned into a circuit of NAND gate chips on a printed circuit board.

To Do:  
- [x] BCD to 7 segment design
- [x] divide by two circuit (t flip flop)
- [x] oscillator circuit design  (pierce oscillator) http://www.ti.com/lit/an/szza043/szza043.pdf
- [x] button debouncing  http://www.ganssle.com/debouncing-pt2.htm
- [ ] or gate block  
- [ ] dimmer(autodimmer? with photoresistor)
- [ ] PWM circuit http://forum.allaboutcircuits.com/threads/project-simple-pwm-circuit.9016/
http://electronics.stackexchange.com/questions/30737/transistors-and-pwm
- [x] power supply circuit
- [ ] LED driver circuit
- [ ] PCB design

Parts List:
74HC00

the 7400 chip
<img src="http://dangerousprototypes.com/blog/wp-content/media/2011/08/7400.jpg">


clock is made up of ~400 NAND gates

made up of 2 main components:
- 31 divide-by-two blocks  
- 4 BCD to 7-Segment Display Decoders
<img src="block-diag.png">

first PCB layout (Dec 20 2016)
<img src="preliminary-PCB.png">

second PCB layout (Jan 4 2016)
<img src= "http://i.imgur.com/Q3IQ6Lw.png">


<img src="http://i.imgur.com/O4u64RL.png">

number display:
<img src="https://statics3.seeedstudio.com/images/product/7%20SegmentL.jpg">

