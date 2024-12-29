# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by:Deepika.V
 RegisterNumber:24000724
*/

module BRC(

input clk,

input reset,

output [3:0]q

);

reg [3:0]q_int;

assign q=q_int;

always@(posedge clk or posedge reset)begin

if(reset)

q_init[0]<=1'b0;

else

q_init[0]<=~q_int[0];

end

genvar i;

generate 

for(i=1;i<4;i=i+1)begin:ripple

always@(posedge q_int[i-1] or posedge reset)begin

if(reset)

q_init[0]<=1'b0;

else

q_init[i]<=~q_int[1];

end

end 

endgenerate 

endmodule

**RTL LOGIC FOR 4 Bit Ripple Counter**
![Screenshot 2024-12-29 192219](https://github.com/user-attachments/assets/3a0233ea-1310-4bb6-adab-51f633ddf2c8)

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
![Screenshot 2024-12-29 192231](https://github.com/user-attachments/assets/7e8ac11b-1844-4b1f-a96e-1aaaeeecbffe)

**RESULTS**
thus the  implementation  4 Bit Ripple Counter using verilog and validating their functionality using their functional tablesus
