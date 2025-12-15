# 4-bit_ripple_counter
# AIM:

To implement 4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:

Quartus prime

# THEORY

4 Bit Ripple Counter

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

<img width="682" height="326" alt="Screenshot 2025-12-16 001239" src="https://github.com/user-attachments/assets/ba1b7a74-377d-4785-a517-21194c515cc6" />

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

<img width="475" height="635" alt="Screenshot 2025-12-16 001250" src="https://github.com/user-attachments/assets/52fa82d1-64dc-413c-842e-d3c1e5d10cab" />


# Procedure

/*1.Increment count on each positive edge of the clock.

2.Reset count to zero when it reaches 15.

3.Generate clock signal (clk).

4.Instantiate the RippleCounter module.

5.Conduct functional testing by displaying the count at each clock cycle for 16 cycles. */


# PROGRAM

# Developed by: HARINI G
# RegisterNumber: 25015377

module bit_ripple_counter (
    input  wire clk,
    input  wire reset,
    output reg [3:0] q
);

    always @(posedge clk or posedge reset) begin
        if (reset)
            q <= 4'b0000;
        else
            q <= q + 1'b1;   
    end

endmodule

# RTL LOGIC FOR 4 Bit Ripple Counter

<img width="1557" height="786" alt="Screenshot 2025-12-15 232425" src="https://github.com/user-attachments/assets/df137cfe-a0e3-46b6-8081-726cfb2ce47c" />

# TIMING DIGRAMS FOR 4 Bit Ripple Counter

<img width="1031" height="567" alt="Screenshot 2025-12-16 001537" src="https://github.com/user-attachments/assets/b5b51b15-fe96-48e8-a640-816993c0d122" />

# RESULTS

Thus 4-BIT-RIPPLE-COUNTER is verified successfully.
