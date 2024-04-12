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
```

module booleanfunction(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and G1(s,ydash,z);
and G2(t,x,y);
and G3(u,w,y);
or G4(f2,s,t,u);
endmodule

```
![image](https://github.com/maddyv123/BOOLEAN_FUNCTION_MINIMIZATION/assets/153618028/4f89b0c6-cd8c-46d0-a46f-8354f10f5d11)

Developed by:MATHAVAN v
register number:212223110026

**Output:**

![image](https://github.com/maddyv123/BOOLEAN_FUNCTION_MINIMIZATION/assets/153618028/b6664f8e-ffac-466b-9461-20fb3a791920)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

