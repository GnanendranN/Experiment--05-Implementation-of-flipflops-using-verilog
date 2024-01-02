# Experiment 05 Implementation of flipflops using verilog
## Name: Gnanendran N
## Register Number: 23006661
# AIM: 
To implement all the flipflops using verilog and validating their functionality using their functional tables
# HARDWARE REQUIRED:
PC, Cyclone II , USB flasher
# SOFTWARE REQUIRED:   
Quartus prime
# THEORY 
## SR Flip-Flop
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

## D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


## JK Flip-Flop
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



## T Flip-Flop
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

# Procedure
 - Using nand gates and wires construct SR flip flop.

 - Repeat same steps to construct JK,D,T flipflops.

 - Find RTL logic and timing diagram for all flipflops.

# PROGRAM 
## SR FlipFlop
![srflipflop](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/ba92aaf0-6551-4f6f-9837-71fc31eb8c58)

## JK FlipFlop
![jkcode](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/7c8824b4-0dc1-44e1-8cff-6803e425e743)

## D FlipFlop
![dflipflop](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/9adccdee-22cf-4e70-a363-2fdc9dcc3ba9)

## T FlipFlop
![tflipflop](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/5747e835-2ce9-4045-b9b7-2888c5661ee1)

# RTL LOGIC FOR FLIPFLOPS 
## SR FlipFlop:
![292388544-0b5b6706-cf1c-425b-b097-2530f695e01a](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/469349e8-6c92-4b15-afaa-7f4137e2eb4f)

## JK FlipFlop:
![jkrtl](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/eab30547-5feb-40cb-8859-b856651f466c)

## D FlipFlop:
![292388603-a0d39d18-26ae-40da-8177-bdac8136d46b](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/b0bc0d1d-d120-4929-9e0e-763081769ef9)

## T FlipFlop:
![292388637-81819c3c-7878-4444-bff2-3341012a7826](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/14c3af8e-af6c-474a-b897-05921005295d)

# Truth Table
## SR FlipFlop
![292388920-25478125-7b39-4604-a941-27d3d29a7060](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/bd2fea77-9dec-4040-b281-293f9fd879c0)

## JK FlipFlop
![292388941-3a104ec4-e988-4225-bc52-a1cd25569b0f](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/3f1688a3-f113-4320-a8e8-a7b834132611)

## D FlipFlop
![292388975-7dabd5e6-b6ec-4fbf-b5bd-c478926a4d12](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/0c5a247d-ec3b-4065-8362-3414e49d4d3f)

## T FlipFlop
![292389011-ac06fe0f-969f-4141-92ba-37ead1e64140](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/41623a9b-b84f-473c-a833-c23e31669636)


# TIMING DIGRAMS FOR FLIP FLOPS 
## SR FlipFlop
![292389059-a3f042c3-da9b-46da-929f-8a3d817933fe](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/e4a07481-54f7-429e-910a-e336aa601f33)

## JK FlipFlop
![292389090-55915d5f-9f60-483a-ab63-19c0f2f2d56e](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/f736add0-6edf-402e-aea5-1ae52279dad0)

## D FlipFlop
![292389123-aa9205a0-ad65-4c24-8efa-289ee68fe53c](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/69893bed-4874-4ca9-aa55-c1d66f7837a1)

## T FlipFlop
![292389173-dadb3250-8c0e-44f2-b81e-c71f0ea1eafd](https://github.com/GnanendranN/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138955207/471beff3-6182-4115-981b-a94c8899598e)

# RESULTS 
Thus, the implementation of SR,JK,D and T flipflops using nand gates are done sucessfully.
