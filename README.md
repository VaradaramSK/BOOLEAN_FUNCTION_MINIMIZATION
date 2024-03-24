# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
module experiment(
    input a, b, c, d, w, x, y, z,
    output f1, f2
);

wire adash, bdash, cdash, ddash, ydash, zdash, wdash;

not(adash, a);

not(bdash, b);

not(cdash, c);

not(ddash, d);

not(ydash, y);

not(zdash, z);

not(wdash, w);

wire p, q, r, s, t, u, term1, term2, term3;

and(p, bdash, ddash);
and(q, adash, b, d);
and(r, a, b, cdash);
and(term1, ydash, z);
and(term2, x, y);
and(term3, w, y);

or(f1, p, q, r);
or(f2, term1, term2, term3);

endmodule


**RTL realization**

**Output:**

**RTL**

**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

