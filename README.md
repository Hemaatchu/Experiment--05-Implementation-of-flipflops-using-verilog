# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.


Developed by: Hemavathy.S
RegisterNumber: 23013552 

## Code:

## SR FLIP FLOP

![SR ff](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/ea91ae5c-b15d-4172-ae96-8dbb0359e756)

## D FLIP FLOP

![exp5 dff](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/09905d5a-f388-4a84-889b-9280d81c39ce)

## JK FLIP FLOP

![exp5 jk ff](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/2b51fb93-9ab8-4431-9e32-2e3791e22179)

## T FLIP FLOP


![T ff (2)](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/3bef4354-595f-4dc8-8705-ce23f2fa04f5)


## Circuit Diagram:

## SR FLIP FLOP

![SR ff (2)](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/bc7c9d8e-68e3-45bb-bddf-9ee395ed1e17)

## D FLIP FLOP

![flipflop](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/a551e49e-77de-432a-a57b-ecaedb626d97)

## JK FLIP FLOP

![JK ff](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/6a03de57-6d84-40d2-bffd-88d1fde31091)

## T FLIP FLOP

![exp 5 t ff](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/051bba95-546c-482e-acb2-b6c8d726548b)

## Truth table:

## SR FLIP FLOP

![exp5 truth table](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/950c91e1-ad1a-4175-9fbc-4ea28fc08a7f)

## D FLIP FLOP

![d ff](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/9ebf0242-d4b6-48c8-b851-ba2c38db1c5e)

## JK FLIP FLOP


![jk tt](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/ddb4d967-7f5f-4102-8123-e29fae86f26a)

## T FLIP FLOP

![T tt](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/51ee34a3-4f3f-470e-8691-2e83b9c8b664)

### Output:

 ## SR FLIP FLOP  
![exp5 output](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/6faafeed-b40f-4fb3-96e9-5248caa3d2c6)


## D FLIP FLOP


![d ff ouput](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/3ff5ccb9-120d-4216-b50e-0026d6551749)

## JK FLIP FLOP


![jk output](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/7384d948-1247-4a7e-9dc9-b8fa72a3260e)

## T FLIP FLOP


![T output](https://github.com/Hemaatchu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147328300/a3e39ca7-623d-4264-b42d-231c714af3af)



### RESULTS 

Thus the SR flipflop, D flipflop, JK flipflop and T flipflop circuits are designed and the truth tables is verified using quartus software.


