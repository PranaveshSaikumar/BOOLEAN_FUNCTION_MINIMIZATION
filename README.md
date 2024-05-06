# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**Program:**

Developed by: Pranavesh Saikumar
RegisterNumber: 212223040149

```
module Boolean_min(A,B,C,D,W,X,Y,Z,F1,F2);
input A,B,C,D,W,X,Y,Z;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
output F1,F2;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign x6=(X)&(~Y)&(Z);
assign x7=(~X)&(~Y)&(Z);
assign x8=(~W)&(X)&(Y);
assign x9=(W)&(~X)&(Y);
assign x10=(W)&(X)&(Y);
assign F1=x1|x2|x3|x4|x5;
assign F2=x6|x7|x8|x9|x10;
endmodule
```

**Truth Table**

![image](https://github.com/PranaveshSaikumar/BOOLEAN_FUNCTION_MINIMIZATION/assets/151001393/7a85c490-0a09-48b3-bc2b-8035c988a1dc)

![image](https://github.com/PranaveshSaikumar/BOOLEAN_FUNCTION_MINIMIZATION/assets/151001393/b6d16493-60be-4562-88c3-655eea698319)

**RTL realization**

![image](https://github.com/PranaveshSaikumar/BOOLEAN_FUNCTION_MINIMIZATION/assets/151001393/f2197f12-a935-4eaa-8e37-90cc98de590d)

**Output:**

![image](https://github.com/PranaveshSaikumar/BOOLEAN_FUNCTION_MINIMIZATION/assets/151001393/5c298bf9-b7dd-453e-8bf7-52db62de0d60)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

