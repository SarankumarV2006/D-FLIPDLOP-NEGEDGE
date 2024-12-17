# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![Screenshot 2024-12-16 224246](https://github.com/user-attachments/assets/e6da88b2-eadf-42cf-9ec7-26a996445e5b)


This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![Screenshot 2024-12-16 225021](https://github.com/user-attachments/assets/fcfcdbf8-7f85-4f88-b45d-a07e1149077d)


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**


1. The Flip-Flop operates with only positive clock transitions.
2. The output of the D Flip-Flop is insensitive to the changes in the input D.
3. The operation of the Flip-Flop is shown in the figure, where the input D and the clock signal (clk) are shown.
4. This circuit has a single input D and two outputs Q and Q'.
5. The outputs Q and Q' only change when a positive transition of the clock signal is applied.

The procedure to understand this logic diagram would be:

1. Understand the basic operation of a Flip-Flop, where the output state changes based on the input and clock signal.
2. Analyze the specific operation of this D Flip-Flop, where the output is insensitive to the changes in the input D, and only the positive clock transitions cause the output to change state.
3. Trace the input D and clock signal (clk) to understand how they affect the output Q and Q'.



**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
Developed by:V.Sarankumar RegisterNumber:24010668
```
module d_flipflop_neg_edge (d, clk, rst, q);
  input d, clk, rst;
  output reg q;

  always @(negedge clk or posedge rst) begin
    if (rst)
      q <= 0; // Reset the flip-flop
    else
      q <= d; // D input is passed to Q on the negative clock edge
  end
endmodule
```


**RTL LOGIC FOR FLIPFLOPS**

**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-12-16 224419](https://github.com/user-attachments/assets/bb95811e-1fd2-4628-92f2-8b558ef64216)


**RESULTS**
Thus the truth table of d flip flop in quartus\\ using verilog programming are studied and verified and executed successfully.
