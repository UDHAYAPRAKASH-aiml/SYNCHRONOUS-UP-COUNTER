### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.
```
**Procedure**
/* write all the steps invloved */:
step 1: first go to qratus prime software
step2: create folder and type the program
step3:In the veriog you get RTL diagram
step4:And the waveform diagram
step 5:end the program 
```
```
**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:udhaya prakash v
RegisterNumber:24901131
module ex11(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule
*/
```
**RTL LOGIC UP COUNTER**:
![Screenshot (57)](https://github.com/user-attachments/assets/d368ef32-06be-42e5-8c04-9f2627a54fd5)



**TIMING DIAGRAM FOR IP COUNTER**:
![ex 11o](https://github.com/user-attachments/assets/a238290c-f096-4153-a71b-33d12b5b2fbe)

TRUTH TABLE:
![t t 11](https://github.com/user-attachments/assets/01858da3-ca88-4e9e-b4e1-1b048160a645)



**RESULTS**:
Thus the up counter are verified.
