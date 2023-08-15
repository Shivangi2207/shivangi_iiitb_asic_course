## Shivangi_iiitb_asic_course

## TAPEOUT PROCESS
 This github repository summarizes the process required  during tapeout.

## Quick links:

[Day 0](#day-0)

[Day 1](#day-1)

[Day 2](#day-2)

[Day 3](#day-3)

[Day 4](#day-4)

[Day 5](#day-5)



[References](#references)

## Day 0
## Yosys

<details>
  <summary><strong>What is yosys?</strong></summary> 
  
  Yosys is a framework for Verilog RTL synthesis.
  It currently has extensive Verilog-2005 support and provides a basic set of     synthesis algorithms for various application domains. 
  Yosys can be adapted to perform any synthesis job by combining the existing passes (algorithms) using synthesis scripts and adding    additional passes as needed by extending the Yosys C++ code base.
  Yosys is free software licensed under the ISC license (a GPL compatible license that is similar in terms to the MIT license or the 
  2-clause BSD license).

</details>

<details>
  <summary><strong>Commands to install Yosys(for linux)</strong></summary> 

```
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys-master
$ sudo apt install make (If make is not installed please install it)
$ sudo apt-get install build-essential clang bison flex
libreadline-dev gawk tcl-dev libffi-dev git
graphviz xdot pkg-config python3 libboost-system-dev
libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make
$ sudo make install
```

![Screenshot from 2023-07-31 09-58-53](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/f0898f77-7e00-41a6-8a96-036bb38a882c)

</details>

## Icarus verilog

<details>
  <summary><strong> What is iverilog? </strong></summary>

Icarus verilog is a compiler that translates Verilog source code into executable programs for simulation, or other netlist formats for further processing. The currently supported targets are vvp for simulation, and fpga for synthesis. 
</details>

<details>
  <summary><strong> Commands to install iverilog</strong></summary>

```

sudo apt-get install iverilog
```

![Screenshot from 2023-07-31 09-59-32](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/6338283f-7296-4109-8ccb-638488b8c950)

</details>

## Gtkwave
<details>
  <summary><strong>What is GTKWave?</strong></summary>

GTKWave is an analysis tool used to perform debugging on Verilog or VHDL
simulation models. With the exception of interactive VCD viewing, it is not
intended to be run interactively with simulation, but instead relies on a post-
mortem approach through the use of dumpfiles. 
</details>

<details>
  <summary><strong>Commands to install gtkwave</strong></summary>

```
$ sudo apt update
$ sudo apt install gtkwave
```
![Screenshot from 2023-07-31 10-00-10](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/5d015986-fa7c-4114-ab27-71e5090eb0b5)
</details>


## Ngspice
<details>
<summary><strong> What is Ngspice?</strong></summary>
	
 Ngspice is the open source spice simulator for electric and electronic circuits.
 Ngspice offers a wealth of device models for active, passive, analog, and digital elements. Model parameters are provided by our       collections, by the semiconductor device manufacturers, or from semiconductor foundries. The user adds her circuits as a netlist, and the output is one or more graphs of currents, voltages and other electrical quantities or is saved in a data file.
</details>

  <details>
<summary><strong>  Installation of Ngspice</strong></summary>

Download the tarball from https://sourceforge.net/projects/ngspice/files/ to a local directory and then follow the commands given below :

## Dependency for Ngspice:
```
$ sudo apt-get install libxaw7-dev
```

## Commands for installation:
```
$ tar -zxvf ngspice-40.tar.gz
$ cd ngspice-40
$ mkdir release
$ cd release
$ ../configure  --with-x --with-readline=yes --disable-debug
$ make
$ sudo make install
```

![Screenshot from 2023-08-02 11-50-49](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/8f533196-cc13-4d60-bb26-73b644097f62)

  
</details>

## Magic
<details>
<summary><strong> What is Magic?</strong></summary>  

Magic is a venerable VLSI layout tool, written in the 1980's at Berkeley by John Ousterhout, now famous primarily for writing the scripting interpreter language Tcl. Due largely in part to its liberal Berkeley open-source license, magic has remained popular with universities and small companies. The open-source license has allowed VLSI engineers with a bent toward programming to implement clever ideas and help magic stay abreast of fabrication technology. However, it is the well thought-out core algorithms which lend to magic the greatest part of its popularity. Magic is widely cited as being the easiest tool to use for circuit layout, even for people who ultimately rely on commercial tools for their product design flow. 

</details>

<details>
<summary><strong> Commands to install Magic</strong></summary>  

```
sudo apt-get install m4
sudo apt-get install tcsh
sudo apt-get install csh
sudo apt-get install libx11-dev
sudo apt-get install tcl-dev tk-dev
sudo apt-get install libcairo2-dev
sudo apt-get install mesa-common-dev libglu1-mesa-dev
sudo apt-get install libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
sudo make install
```
![Screenshot from 2023-08-02 10-40-41](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/72965e3d-5ae9-4ceb-83d9-04ea78a89492)




</details>

## OpenSTA
<details>
<summary><strong>What is OpenSTA?</strong></summary>

OpenSTA is a distributed software testing architecture designed around CORBA, it was originally developed to be commercial software by CYRANO. The current toolset has the capability of performing scripted HTTP and HTTPS heavy load tests with performance measurements from Win32 platforms. However, the architectural design means it could be capable of much more.
</details>

<details>
<summary><strong>Commands to install OpenSTA</strong></summary>

## Steps:
Prior to the installation of the OpenSTA install the dependencies using the command shown below :
```
sudo apt-get install cmake clang gcc tcl swig bison flex 
```

After installing the dependencies use the following command to install OpenSTA:

```
git clone https://github.com/The-OpenROAD-Project/OpenSTA.git
cd OpenSTA
mkdir build
cd build
cmake ..
make
sudo make install
```

![Screenshot from 2023-08-02 11-44-43](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/d5b824eb-4c7b-4453-8d68-65950d9b69fd)


  
</details>

## OpenLANE
<details>
<summary><strong>What is OpenLANE?</strong></strong></summary> 

OpenLane is an automated RTL to GDSII flow based on several components including OpenROAD, Yosys, Magic, Netgen, CVC, SPEF-Extractor, KLayout and a number of custom scripts for design exploration and optimization. It also provides a number of custom scripts for design exploration and optimization.
OpenLane abstracts the underlying open source utilities, and allows users to configure all their behavior with just a single configuration file.
</details>

<details>
<summary><strong>Installation of OpenLANE</strong></strong></summary> 

Prior to the installation of the OpenLane install the dependencies and packages using the command shown below :

```
sudo apt-get update
sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv python3-pip make git
```

## Docker Installation

```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world

sudo groupadd docker
sudo usermod -aG docker $USER
sudo reboot 


# Check for installation
sudo docker run hello-world
```

## Steps to install OpenLane, PDKs and Tools

```
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test
```
</details>



## Day 1

## Summary
<details>
<summary><strong>Day_1_intro</strong></summary>
 
In todays Lab i have done simulation and synthesis of 2x1 Mux  using iverilog and yosys respectively. iverilog generates from the RTL design and its testbench a value changing dump file (vcd). gtkwave is the tool used to plot the simulation results of the design.

## Simulator
Simulator is the tool used for simulating the design.Here we have used iverilog. RTL design is checked for adherence to the specs by simulting the design.It changes on input signals.Only when the input changes the output is evaluated.

## RTL Design
Design is the actual code or set of verilog codes which has the intended functionality to meet with the required specifications.It may have 1 or more primary inputs and outputs.
## Testbench
Testbench is the setup to apply stimulus to the design to check its functionality.It does not have any primary i/p or o/p.

![Screenshot from 2023-08-09 10-00-22](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/68b1864c-7690-4f67-a25b-b798957bbdde)


## Synthesizer
It is a tool which is used for converting the RTL To netlist.Here we have used Yosys for synthesizer. In this we use same testbench that we have used during simulation to verify the synthesis.The design is converted into gates and the connections are made between the gates.This is given out as a file called netlist.

<img src="https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/3e2c91f3-9abc-4367-8201-da4faf13b052" alt="alt text" width="400" height="400">

## .lib 
Lib file is a short form of Liberty Timing file. Liberty syntax is followed to write a .lib file. It is a collection of logical modules. It includes basic logic gates like And, Or,Not etc. It contains different flavours of gate (slow,fast,medium).

<img src="https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/20e36961-74b3-4eeb-b183-a798594a00ad" width="400" height="400">


So based on our requirement we use different flavours of cell.

a) Faster the cells lesser is the delay, but for that we need wider transistors      so the power dissipation will be more too.So faster cells donot come free,they    come at penalty of area and power.More use of faster cell will result in bad      circuit with large area and power dissipation.

b) slower cells are used at non-critical path where we donot require high            performance where delay is not an issue so our power dissipation and area will    also be minimum. But more use of slower cells will make our circuit sluggish.



      
</details>

## Verilog code
<details>
<summary><strong>Verilog code</strong></summary>
The verilog codes of the 2x1 mux (good_mux.v) and its testbench (tb_good_mux.v) are taken from https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git


## Commands to download the lab folder

```
$ git clone https://github.com/kunalg123/vsdflow.git
$ git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git


```   

 
## Verilog code of good_mux.v and tb_good_mux.v

## Design file
```

module good_mux (input i0 , input i1 , input sel , output reg y);
always @ (*)
begin
	if(sel)
		y <= i1;
	else 
		y <= i0;
end
endmodule

```
## Test bench

```

`timescale 1ns / 1ps
module tb_good_mux;
	// Inputs
	reg i0,i1,sel;
	// Outputs
	wire y;

        // Instantiate the Unit Under Test (UUT)
	good_mux uut (
		.sel(sel),
		.i0(i0),
		.i1(i1),
		.y(y)
	);

	initial begin
	$dumpfile("tb_good_mux.vcd");
	$dumpvars(0,tb_good_mux);
	// Initialize Inputs
	sel = 0;
	i0 = 0;
	i1 = 0;
	#300 $finish;
	end

always #75 sel = ~sel;
always #10 i0 = ~i0;
always #55 i1 = ~i1;
endmodule

```
</details>

## Simulation
<details>
<summary><strong>Commands</strong></summary>
To simulate and view plots of 2x1 mux (good_mux.v) and its testbench (tb_good_mux.v) following commands are used:

```
$ iverilog good_mux.v tb_good_mux.v
$ ./a.out
$ gtkwave tb_good_mux.vcd

```
</details>

<details>
<summary><strong>Plot obtained:</strong></summary>

![Screenshot from 2023-08-08 23-47-03](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/5083f91b-52f1-4343-94de-353008bd834b)

</details>


##  Synthesis
<details>
<summary><strong>Commands</strong></strong></summary>
 

In the directory of verilog_files (/home/shivangi/VLSI/sky130RTLDesignAndSynthesisWorkshop/verilog_files) following commands are used to synthesize and view Synthesized design :

```
$ yosys
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog good_mux.v
synth -top good_mux
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> show
```
</details>


<details>
<summary><strong>Synthesized design</strong></strong></summary>

![Screenshot from 2023-08-09 00-09-18](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/16ddbc34-90bb-47ba-809c-2fed1fa67731)

</details>

<details>
<summary><strong>Generation of netlist</strong></strong></summary>


Now, to generate the netlist following commands are used:

```
yosys> write_verilog good_mux_netlist.v
yosys> write_verilog -noattr good_mux_netlist.v
yosys> !gvim good_mux_netlist.v 

```

![Screenshot from 2023-08-09 10-02-49](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/9e260074-ba0a-4f5e-8629-7195665ac8ad)

</details>

<details>
<summary><strong>Generated Netlist</strong></strong></summary>

![Screenshot from 2023-08-09 00-18-20](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/22c8fd55-79f5-4f7d-b58d-04b4f8dc837b)

      
</details>

## Day 2
## Summary
<details>
<summary><strong>Day_2_intro</strong></summary>
In todays lab I have learnt about .lib file and different flavours of gate present in .lib file.
Along with that i have synthesized a multiple module (made of two submodules) at the multiple module level (both in hierarchical and flattened forms) then at the submodule level. 
//complete it

## .lib file
We have used sky130_fd_sc_hd__tt_025C_1v80.lib file. The name of the .lib file represent different parameter as follows:

tt- typical process

025C- temperature

1v80-voltage

![Screenshot from 2023-08-14 21-50-52](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/a565ec55-5300-4a98-aff7-e68959c89ec2)

Now .lib file also contains different flavours of gate modules. lets look through some different and gate module present in our .lib file

 ![Screenshot from 2023-08-14 21-56-11](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/1235470d-8fb3-4712-b864-7d9046ecd3fb)

 As shown in the above fig. three types of gate module are there we have and2_0 , and2_2, and2_4. If we carefully look into the figure we will see that the area is less for the 1st one and largest for the 3rd one.So and0_4 is the wide transistor and and2_0 is the narrow one so the and0_4 will be fastest and and2_0 is the slowest and performance of the middle one  is in betwwen these two transistors. So according to our own requirement we will choose what to use and where to use these modules. 

</details>

## Hierarchical vs Flat synthesis

<details>
	<summary><strong>Hierarchical synthesis</strong></summary>
 Lets understand the sysnthesis with the of an example. I have synthesized a mutiple_modules.v file whose code is given below. In this we have multiple_modules as a top module in which we have instatiated sub_module1 and sub_module2 which performs And operation and or operation respectively.

```
module sub_module2 (input a, input b, output y);
	assign y = a | b;
endmodule

module sub_module1 (input a, input b, output y);
	assign y = a&b;
endmodule

module multiple_modules (input a, input b, input c , output y);
	wire net1;
	sub_module1 u1(.a(a),.b(b),.y(net1));  //net1 = a&b
	sub_module2 u2(.a(net1),.b(c),.y(y));  //y = net1|c ,ie y = a&b + c;
endmodule
```

Then I synthesized the file using following commands:
```
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> read_verilog multiple_modules.v
yosys> synth -top multiple_modules
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> show multiple_modules 

```

This is the schematic as per the port connection in th above module.
![IMG_20230814_225311](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/6f8e28e9-b723-4421-81d8-d415a3acd52b)

Commands to get the hierarchical netlist:
```
yosys> write_verilog -noattr multiple_modules_hier.v
yosys> !gvim  multiple_modules_hier.v
```
However we get the following schematic instead of the above one. 
![Screenshot from 2023-08-14 22-43-12](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/39e5911f-865c-4a80-b41e-1fcc4d6f9349)

This is what we call hierarchical design.The synthesizer considers the module hierarcy and does the mapping accordting to instantiation. Here is the hierarchical netlist code for the multiple_modules:

```
module multiple_modules(a, b, c, y);
	  input a;
	 input b;
	 input c;
	  wire net1;
	 output y;
  sub_module1 u1 (.a(a),.b(b),.y(net1) );
  sub_module2 u2 (.a(net1),.b(c),.y(y));
endmodule

module sub_module1(a, b, y);
 wire _0_;
 wire _1_;
 wire _2_;
 input a;
 input b;
 output y;
 sky130_fd_sc_hd__and2_0 _3_ (.A(_1_),.B(_0_),.X(_2_));
 assign _1_ = b;
 assign _0_ = a;
 assign y = _2_;
endmodule

module sub_module2(a, b, y);
wire _0_;
 wire _1_;
 wire _2_;
input a;
input b;
 output y;
 sky130_fd_sc_hd__lpflow_inputiso1p_1 _3_ (.A(_1_),.SLEEP(_0_),.X(_2_) );
 assign _1_ = b;
 assign _0_ = a;
 assign y = _2_;
endmodule
```

## Flat synthesis

In the flat synthesis hierarchies are flattened out and directly instantiates gates here. The flattened netlist is given below.

```

module multiple_modules(a, b, c, y);
      wire _0_;
      wire _1_;
      wire _2_;
      wire _3_;
      wire _4_;
      wire _5_;
      input a;
      wire a;
      input b;
      wire b;
      input c;
      wire c;
      wire net1;
      wire \u1.a ;
      wire \u1.b ;
      wire \u1.y ;
      wire \u2.a ;
      wire \u2.b ;
      wire \u2.y ;
      output y;
      wire y;
  sky130_fd_sc_hd__and2_0 _6_ (
            .A(_1_),
            .B(_0_),
            .X(_2_)
              );
  sky130_fd_sc_hd__or2_0 _7_ (
            .A(_4_),
            .B(_3_),
            .X(_5_)
              );
  assign _4_ = \u2.b ;
  assign _3_ = \u2.a ;
  assign \u2.y  = _5_;
  assign \u2.a  = net1;
  assign \u2.b  = c;
  assign y = \u2.y ;
  assign _1_ = \u1.b ;
  assign _0_ = \u1.a ;
  assign \u1.y  = _2_;
  assign \u1.a  = a;
  assign \u1.b  = b;
  assign net1 = \u1.y ;
endmodule
```
The commands for flat synthesis are:
```
yosys> flatten
yosys> write_verilog -noattr multiple_modules_flat.v
yosys> !vim multiple_modules_flat.v
```
This is the synthyesized circuit for a flattened netlist. Here u1 and u2 are flattened and directly or gates are realized.

![Screenshot from 2023-08-15 00-45-04](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/3dcc2b79-a888-470b-b888-9667f159a82a)

</details>



## Why flops?

Flip-flops are used as memory elements in sequential circuit. The output is obtained in a sequential circuit from combinational circuit or flip-flop or both. The state of flip-flop changes at active state of clock pulses and remains unaffected when the clock pulse is not active.Flip-flops are the quintessential edge-triggered logic. Along with the fact that they have memory, this makes them the gate-keeper component that can block when there is no clock edge, sample signals on the clock edge, and preserve the output signal away from a clock edge. Flip-flops allow the the clock control the flow of signals from one component to the next.

<details>
<summary><strong>Flipflop simulation and synthesis</strong></summary>

## Asynchronous reset flipflip

```
module dff_asyncres_syncres ( input clk , input async_reset , input sync_reset , input d , output reg q );
always @ (posedge clk , posedge async_reset)
begin
	if(async_reset)
		q <= 1'b0;
	else if (sync_reset)
		q <= 1'b0;
	else	
		q <= d;
end
endmodule
```
Simulation:

![Screenshot from 2023-08-15 10-48-40](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/eb2154ac-51bc-4743-abb0-a4c4bb2d4f58)

Here the output q goes low whenever reset is high and will not wait for the clock's posedge, i.e irrespective of clock, the output is changed to low.

## Synthesis

commands:
```
$yosys
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog dff_asyncres.v
yosys> synth -top dff_asyncres
yosys> dfflibmap -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> show
```
Design obtained with active high reset

## Synthesized circuit:

![Screenshot from 2023-08-15 11-08-40](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/754f9c96-60ca-41eb-a94f-47b08622417c)

## Asynchronous set d flipflop

```
module dff_async_set ( input clk ,  input async_set , input d , output reg q );
always @ (posedge clk , posedge async_set)
begin
	if(async_set)
		q <= 1'b1;
	else	
		q <= d;
end
endmodule

```
## Simulation

![Screenshot from 2023-08-15 10-52-36](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/7e89ef11-e8c1-44f8-92b2-62d7113e1bf0)



 Here the output q goes high whenever set is high and will not wait for the clock's posedge, i.e irrespective of clock, the output is changed to high.

 ## Synthesis
 commands
 ```
$yosys
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog dff_async_set.v 
yosys> synth -top dff_async_set
yosys> dfflibmap -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> show
```
## Synthesized circuit:

![Screenshot from 2023-08-15 11-12-22](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/8e3d6e87-0d20-489b-8b36-2e491667ea3f)


## Synchronous reset
```
module dff_syncres ( input clk , input async_reset , input sync_reset , input d , output reg q );
always @ (posedge clk )
begin
	if (sync_reset)
		q <= 1'b0;
	else	
		q <= d;
end
endmodule
```
## Simulation:

 ![Screenshot from 2023-08-15 10-58-17](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/683a4cab-630d-4def-853a-63175fb6ed64)

Here the output q goes low whenever reset is high and at the positive edge of the clock. Here the reset of the output depends on the clock.

## Synthesis

commands
```

$yosys
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog dff_syncres.v 
yosys> synth -top dff_syncres
yosys> dfflibmap -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> show
```


## Synthesized circuit:
![Screenshot from 2023-08-15 11-22-05](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/63033669-59ea-4673-80d3-d8861c2d9aba)


## Dff with both synchronous and asynchronous reset
```
module dff_asyncres_syncres.v ( input clk , input async_reset , input sync_reset , input d , output reg q );
always @ (posedge clk , posedge async_reset)
begin
	if(async_reset)
		q <= 1'b0;
	else if (sync_reset)
		q <= 1'b0;
	else	
		q <= d;
end
endmodule

```

## Simulation

![Screenshot from 2023-08-15 11-31-42](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/8089ae2a-10b3-4b9f-b4c4-d53181373aac)

Here the output q goes low whenever asynchronous reset is high where output doesn't depend on clock and also when synchronous reset is high and posedge of clock occurs.

## Synthesis

commands
```

$yosys
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog dff_asyncres_syncres.v
yosys> synth -top dff_asyncres_syncres
yosys> dfflibmap -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> show

```

## Simulation
![Screenshot from 2023-08-15 11-30-15](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/62ff37ff-89aa-4d17-b44d-4de34f44bf6f)


## Some interseting Optimisation
In this we have deal with some automatic and intersetion optimisation. Here are some examples: Like multiplying a number with 2 does not need any hardware and only can be done by adding 0's in the a like if we multiply it by 4 then we will add 2 0's from back and for multiplication with 8 we have to add three 0's to a from back. 

## Code
```
module mul2 (input [2:0] a, output [3:0] y);
	assign y = a * 2;
endmodule
```
## Netlist for the above Schematic:
```
module mul2(a, y);
  input [2:0] a;
  wire [2:0] a;
  output [3:0] y;
  wire [3:0] y;
  assign y = { a, 1'h0 };
endmodule
```
## Synthesized circuit:

![Screenshot from 2023-08-15 12-02-19](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/20284045-da51-471e-8f25-034c8f0b2432)

Multiplication by 8
 

## Schematic


![Screenshot from 2023-08-15 12-08-36](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/a699daf3-2a2b-468b-9e6d-e45118501a1c)

## Netlist for the above Schematic:
```
module mult8(a, y);
  input [2:0] a;
  wire [2:0] a;
  output [5:0] y;
  wire [5:0] y;
  assign y = { a, a };
endmodule
```


</details>



## Day 3

## Optimisation

Logic optimization is a process of finding an equivalent representation of the specified logic circuit under one or more specified constraints. This process is a part of a logic synthesis          applied in digital electronics and integrated circuit design. 
There are two types of optimisation logic

 ## What Combinational logic optimisation?
 
<details><summary><strong>Combinational logic optimisation with example</strong></summary><br>
 	In this the logic gates get squeezed  to get the most optimized design that results in area and power saving.
  It is done by two means:
  
## 1. Constant propagation logic optimisation
  
  Constant Propagation is an optimization technique employed by synthesis tools to minimize hardware implementation. This is achieved by optimizing away the logic for which parameters are configured to keep it disabled.

let's understand it by an example:

In this example we fixed one of our input A to 0 then progate it to the output. So we can simply replace the whole big circuit with just and inverter as both are having same output.

![IMG_20230815_131136](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/f21a189f-ccb8-4959-99a9-406fd5a07898)

## 2.Boolean logic optimisation

The optimization methods that consider logic functions as well as their representations are called "Boolean methods"
Boolean function minimizing methods include: 
 a. Karnaugh maps
 b. Quine–McCluskey algorithm

 let's understand it by an example:
 In this optimisation we basically try to reduce the boolean expression using required methods.Hence we get the reduced logic expression 
 
![IMG_20230815_131122](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/7298588e-8a12-4a10-838b-2085b225d765)

Here we will be doing the labs that illustrate combinational logic optimizations.

## Example 1:
## Code
```
module opt_check (input a , input b , output y);
	assign y = a?b:0;
endmodule
```

## Commands to run
```
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog opt_check.v
yosys> synth -top opt_check
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> show
```
## Obtained schematic
 
 ![Screenshot from 2023-08-15 15-58-12](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/b7a9d8b3-77e6-4d9b-ac4f-4e1fc317b8af)

## Example 2:
## Code

```
module opt_check2 (input a , input b , output y);
	assign y = a?1:b;
endmodule
```

## Commands:
```
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog opt_check2.v
yosys> synth -top opt_check2
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> show

```
## Obtained schematic
![Screenshot from 2023-08-15 16-05-53](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/81414174-421d-414b-bb57-6f178b678d91)

## Example 3:
## Code
```
module opt_check3 (input a , input b, input c , output y);
	assign y = a?(c?b:0):0;
endmodule
```
## Commands:
```
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog opt_check3.v
yosys> synth -top opt_check3
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> show


```
## Obtained schematic

![Screenshot from 2023-08-15 16-11-55](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/c32afba8-6da7-4ac4-907d-030f61cec27e)

## Example 4:
## Code
```
module opt_check4 (input a , input b , input c , output y);
	assign y = a?(b?(a & c ):c):(!c);
endmodule
```

##  Commands
```
yosys> read_liberty -lib ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> read_verilog opt_check4.v
yosys> synth -top opt_check4
yosys> abc -liberty ../my_lib/lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> show
```
## Obtained schematic

![Screenshot from 2023-08-15 16-17-10](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/e7724271-df4e-4da0-bdbb-e1823f45b7a4)

## Example 5:
## Code
```
module sub_module(input a , input b , output y);
	assign y = a & b;
endmodule

module multiple_module_opt2(input a , input b , input c , input d , output y);
	wire n1,n2,n3;
	sub_module U1 (.a(a) , .b(1'b0) , .y(n1));
	sub_module U2 (.a(b), .b(c) , .y(n2));
	sub_module U3 (.a(n2), .b(d) , .y(n3));
	sub_module U4 (.a(n3), .b(n1) , .y(y));
endmodule
```


## Commands
```
yosys:read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys:read_verilog multiple_module_opt2.v
yosys:synth -top multiple_module_opt2
yosys:abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys:flatten
yosys:opt_clean -purge
yosys:show

```
## Before flatten

![Screenshot from 2023-08-15 16-27-08](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/353b02c6-d5f0-4a28-ae4f-4eed22e3b5ce)



## After Flatten


![Screenshot from 2023-08-15 16-24-37](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/14ba880d-2539-4801-9d3a-b5d7ee74401d)


## Example 6:
## Code
```
	module sub_module1(input a , input b , output y);
	 assign y = a & b;
	endmodule

	module sub_module2(input a , input b , output y);
	 assign y = a^b;
	endmodule

	module multiple_module_opt(input a , input b , input c , input d , output y);
	wire n1,n2,n3;
	sub_module1 U1 (.a(a) , .b(1'b1) , .y(n1));
	sub_module2 U2 (.a(n1), .b(1'b0) , .y(n2));
	sub_module2 U3 (.a(b), .b(d) , .y(n3));

	assign y = c | (b & n1); 
	endmodule
```
## Commands
```
yosys:read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys:read_verilog multiple_module_opt.v
yosys:synth -top multiple_module_opt
yosys:abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys:flatten
yosys:opt_clean -purge
yosys:show

```
## Before flatten
![Screenshot from 2023-08-15 16-30-20](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/5780d3be-a35a-4846-b400-2ed25ad80c00)


## After Flatten
![Screenshot from 2023-08-15 16-30-59](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/60d32fb1-0ace-433d-8acf-409436635091)



 </details>

 ## What is Sequential logic optimisation?
 
<details>
<summary><strong>Sequential logic optimisation with example</strong></summary>
sequential logic optimization method has been presented that is based on selectively precomputing the output logic values of the circuit one clock cycle before they are required, and using the precomputed values to reduce internal switching activity in the succeeding clock cycle
It is done by various means:
1. sequential constant propagation
Let's understand this using an example

![IMG_20230815_145417](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/191cb347-68d8-432e-bab3-9316295bb3b4)

In the 1st Dff Q will always be 0 when reset is high Q become 0 also when reset is not high it will be 0 again as D is grounded . So Q=0 is propagated to nand gate so our output will always be 1. But this is not the case with the 2nd Dff as in this Q=1 when set is high and Q=0 when set is not applied and D is grounded.

So in the 1st Dff Q pin is constant so it can be optimised furthur , but  the 2nd Dff can't be optimised as its Q pin is not constant.

## 1. State optimisation:

In this optimisation of unused states are done.

## 2. Cloning:

This is done when performing PHYSICAL AWARE SYNTHESIS. Lets consider a flop A which is connected to flop B and flop C through a combination logic. If B and C are placed far from A in the flooerplan, there is a routing path delay. To avoid this, we connect A to two intermediate flops and then from these flops the output is sent to B and C thereby decreasing the delay. This process is called cloning since we are generating two new flops with same functionality as A.


## 3.Retiming: 
Retiming is a powerful sequential optimization technique used to move registers across the combinational logic or to optimize the number of registers to improve performance via power-delay trade-off, without changing the input-output behavior of the circuit. 

## Example 1:
Here flop will be inferred as the output is not constant.

```
module dff_const1(input clk, input reset, output reg q);
	always @(posedge clk, posedge reset)
	begin
		if(reset)
			q <= 1'b0;
		else
			q <= 1'b1;
	end
endmodule
```
## Simulation
![Screenshot from 2023-08-15 16-46-23](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/7c9a0178-a773-4a6e-81e6-f3a7a9b506b9)

## Synthesis
![Screenshot from 2023-08-15 17-16-56](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/c2fd5e40-a46a-44de-ac10-11ed46f921da)

![Screenshot from 2023-08-15 17-18-26](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/65d7dab5-d87a-4f81-8a5e-ee2298e46896)


## Example 2:


## Code
```
module dff_const2(input clk, input reset, output reg q);
	always @(posedge clk, posedge reset)
	begin
		if(reset)
			q <= 1'b1;
		else
			q <= 1'b1;
	end
endmodule
```
## Simulation

![Screenshot from 2023-08-15 16-53-35](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/1b8dd043-b983-4b1c-9aa5-a9404a475430)

## Synthesis
![Screenshot from 2023-08-15 17-20-43](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/6122a530-114b-4821-93eb-7c748f57564b)

![Screenshot from 2023-08-15 17-21-17](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/53e451b4-e77b-4530-ae60-8bc1cb2834d2)


## Example 3:

## Code
```
	module dff_const3(input clk, input reset, output reg q);
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b1;
			q1 <= 1'b0;
		end
		else
		begin
			q1 <= 1'b1;
			q <= q1;
		end
	end
	endmodule
```
 ##  Simulation
![Screenshot from 2023-08-15 16-56-35](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/a38c62ad-f15e-4bf3-8fcb-2b276689f272)


 ## Synthesis

 ![Screenshot from 2023-08-15 17-22-33](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/26e3085e-8064-4475-9f0f-a0dad5cc20bc)


![Screenshot from 2023-08-15 17-22-59](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/a373dfe9-682a-4b0f-b966-d20f25599dad)

 ## Example 4:
 ## Code
 ```
	module dff_const4(input clk, input reset, output reg q);
	reg q1;

	always @(posedge clk, posedge reset)
	begin
		if(reset)
		begin
			q <= 1'b1;
			q1 <= 1'b1;
		end
	else
		begin
			q1 <= 1'b1;
			q <= q1;
		end
	end
	endmodule
```
## Simulation
![Screenshot from 2023-08-15 16-57-36](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/30c4cbee-240a-4cbf-ba9b-5a536f92446c)


## Synthesis
![Screenshot from 2023-08-15 17-24-09](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/8bd694a1-23be-4cfd-a796-294d895e914c)


![Screenshot from 2023-08-15 17-24-26](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/805c84bc-a27d-4e36-88fa-3072ef5d294b)


## Example 5:
## Code 
```
	module dff_const5(input clk, input reset, output reg q);
	reg q1;
	always @(posedge clk, posedge reset)
		begin
			if(reset)
			begin
				q <= 1'b0;
				q1 <= 1'b0;
			end
		else
			begin
				q1 <= 1'b1;
				q <= q1;
			end
		end
	endmodule
```
## Simulation

![Screenshot from 2023-08-15 17-00-45](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/d3f13139-1ed9-4a11-9bc3-4534ac29e822)

## Synthesis

![Screenshot from 2023-08-15 17-25-07](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/fda7987c-7209-4e89-a1c6-60b7457f740c)

![Screenshot from 2023-08-15 17-25-25](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/767eb92d-8dbd-4866-a345-3512ce7a2cba)

 
</details>

 


<details>
<summary><strong>Sequencial optimisation for unsed outputs </strong></summary>


## Example 1:
## Code
```
	module counter_opt (input clk , input reset , output q);
	reg [2:0] count;
	assign q = count[0];
	always @(posedge clk ,posedge reset)
	begin
		if(reset)
			count <= 3'b000;
		else
			count <= count + 1;
	end
	endmodule
```

## Synthesis

![Screenshot from 2023-08-15 17-33-27](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/4a56108d-b247-4418-bfe0-384a15299886)

 ![Screenshot from 2023-08-15 17-32-24](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/c4223175-5c4c-4d37-9c98-295452cb4ff8)


 ## Example 2:
 Updated Counter logic:
 ```
module counter_opt (input clk , input reset , output q);
	reg [2:0] count;
	assign q = {count[2:0]==3'b100};
	always @(posedge clk ,posedge reset)
	begin
	if(reset)
		count <= 3'b000;
	else
		count <= count + 1;
	end
endmodule
```

 ## Synthesis
 
 ![Screenshot from 2023-08-15 17-43-21](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/2839f35f-9f10-4c31-b731-650b605779ca)

![Screenshot from 2023-08-15 17-39-28](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/e885ec04-0c4e-41fe-9780-a1115d339aa2)


</details>

## Day 4


<details>
<summary><strong>GLS</strong></summary><br>

## GLS
	
1. We will run the test bench with netlist as design under test.
2. Netlist is logically same as RTL code.
3. Gate level verilog models can be timing aware or functional.

## Why GLS?

To verify the logical correctness of the design after synthesis
   
To meet the timing requirements of the design, this is done using delay annotation.
   
To test the funcionality of the netlist because there can be synthesis-simulation mismatch

## GLS using iverilog

If the Gate Level Models are delay annotated,then we can use GLS for timing validation

![Screenshot from 2023-08-15 18-12-11](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/97a73bbe-7aac-4156-aa9f-e863ea2b9456)

## Synthesis Simulation Mismatch

Synthesis simulation mismatch refers to a discrepancy or misalignment between the expected behavior of a system or device, as predicted by a simulation or modeling process, and the actual behavior observed in the physical implementation or real-world operation of that system or device. This term is often used in fields such as electronics, engineering, and computer science, where simulations are employed to model the behavior of complex systems before they are physically constructed or deployed.

There are three main reasons for Synthesis Simulation Mismatch:

## 1 Missing sensitivity list in always block:

In below code there is a sensitivity mismatch
As  always block will execute only when sel changes so the block inside will not execute to give proper output of a mux 

![Screenshot from 2023-08-15 18-23-02](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/d306ad6d-2da3-4f48-b479-0d2af150094a)

## 2 Blocking vs Non-Blocking Assignments:
Blocking statements execute the statemetns in the order they are written inside the always block. Non-Blocking statements execute all the RHS and once always block is entered, the values are assigned to LHS. This will give mismatch as sometimes, improper use of blocking statements can create latches. 

3 Non standard Verilog coding

</details>
<details>
<summary><strong>Labs on GLS and Synthesis-Simulation Mismatch
</strong></summary>

## Example 1:
```
module ternary_operator_mux (input i0 , input i1 , input sel , output y);
	assign y = sel?i1:i0;
endmodule
```
## Simulation



 ![Screenshot from 2023-08-15 19-01-24](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/35015884-20b4-49eb-989d-4c95c3f86d96)

## Synthesis
![Screenshot from 2023-08-15 19-06-06](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/8f628a0c-5a6f-4acc-996f-28fc625d2584)


 ![Screenshot from 2023-08-15 19-07-49](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/0237a8e3-b176-4726-85cc-b5b20f6d3650)

 ## Netlist Simulation
 ![Screenshot from 2023-08-15 19-24-44](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/bffd8e42-0e83-41db-bc9f-aa16a5dbafdb)

As we can see there is no mismatch in  the simulation.

## Example 2:
## Code
```
module bad_mux (input i0 , input i1 , input sel , output reg y);
	always @ (sel)
	begin
		if(sel)
			y <= i1;
		else 
			y <= i0;
	end
endmodule
```
## Simulation

![Screenshot from 2023-08-15 19-31-45](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/a7260a44-29e0-4264-9358-3e24d103e2b8)

## Synthesis
![Screenshot from 2023-08-15 19-34-57](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/63053bd8-342d-447a-8792-43c96a526f77)

![Screenshot from 2023-08-15 19-41-52](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/756123eb-1a32-406b-8e1a-6a8e12d48c9f)

## Netlist Simulation
![Screenshot from 2023-08-15 19-39-25](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/df1c42c5-ef7e-4b50-94d7-733459ece727)

Here first pic shows the netlist simulation which corrects the bad_mux design which was only changing waveform when sel was triggered while for a mux to work properly it should be sensitivity to all the input signals



</details>
<details>
<summary><strong>Labs on synth-sim mismatch for blocking statement
</strong></summary>

Here the output is depending on the past value of x which is dependednt on a and b and it appears like a flop.

## Example 1:
```
module blocking_caveat (input a , input b , input  c, output reg d); 
reg x;
always @ (*)
	begin
	d = x & c;
	x = a | b;
end
endmodule
```
## Simulation

![Screenshot from 2023-08-15 19-50-51](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/a310caf4-0a6a-4ee5-84a1-892dafa6e6b7)


## Synthesis

![Screenshot from 2023-08-15 19-51-48](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/6564e452-66c6-4a81-b1fd-6944d2450320)

![Screenshot from 2023-08-15 19-52-16](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/da278c5c-4061-4b95-ba4d-8349130ea1ee)


## Netlist simulation

 ![Screenshot from 2023-08-15 19-53-52](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/8d3a2da1-d37a-4255-8dcb-15c8af9c35a2)

 Here this how the circuit should behave but this correct waveform is only obtained while doing netlist simulation. Here first pic show the netlist simulation which shows the proper working of the dut while the last pic shows the improper working of dut as we have used blocking statement here which causes synthesis simulation mismatch which is sorted out by GLS while providing netlist simulation

</details>

## Day 5

<details>
	<summary><strong> If Case constructs</strong>
	</summary>

 ## IF Statement
If statement is used to conditionally execute a block of code based on a given condition.

## Syntax
```
if (condition)
    // Code to be executed if the condition is true
else
    // Code to be executed if the condition is false
```
	
## Precautions with "If"
Due to incomplete if statements i.e. when we use "if" without "else" statements, it inferes latches which affects the working of code. But there are some conditions where we require latches like counters.

## Case Statement
It is used in "always" block.
Variable which is used in case statement should be a reg.

## Syntax
```
 case(choice)
   choice1: begin
   --------
   --------
   end
   choice2: begin
   --------
   --------
   end
   default: <statements>
 endcase
```
## Precautions with "Case"

Incomplete case also inferes latches and to avoid that we should use default statement in case.
Partial Assignments: If some of the outputs are not assigned any value in some of the segments of case then it inferes latches which can affect the working of code.
We should not have overlapping cases as unlike "If" statements no priority is given to any condition hence it will check all the cases even if it matches the one condition, which in return gives unpredictable outputs.



</details>

<details>
	<summary><strong>Labs on "Incomplete If Case"</strong></summary>

 ## Example 1:
```
module incomp_if (input i0 , input i1 , input i2 , output reg y);
always @ (*)
begin
	if(i0)
		y <= i1;
end
endmodule
```
## Simulation
![Screenshot from 2023-08-15 20-29-55](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/c6fccfc4-09f1-4737-823b-c68210fdb7c4)


## Synthesis

```
yosys
yosys> read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> read_verilog incomp_if.v 
yosys> synth -top incomp_if
yosys> abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> write_verilog -noattr incomp_if_net.v
yosys> show
```

![Screenshot from 2023-08-15 20-35-00](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/a741528b-6eea-4b64-a38c-158ef33980bf)

![Screenshot from 2023-08-15 20-35-23](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/df31b037-23b6-4d50-bea7-9d4a458be790)


## Example 2:
```
module incomp_if2 (input i0 , input i1 , input i2 , input i3, output reg y);
	always @ (*)
	begin
		if(i0)
			y <= i1;
		else if (i2)
			y <= i3;
	end
endmodule
```
## Simulation
![Screenshot from 2023-08-15 20-39-58](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/3f6f4348-7ebc-40ab-8360-b64dec64caa9)


## Synthesis
```
yosys
yosys> read_liberty -lib ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib 
yosys> read_verilog incomp_if2.v 
yosys> synth -top incomp_if2
yosys> abc -liberty ../lib/sky130_fd_sc_hd__tt_025C_1v80.lib
yosys> write_verilog -noattr incomp_if2_net.v
yosys> show
```

![Screenshot from 2023-08-15 20-40-45](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/da9d3596-d78e-4a79-ace0-45957e894a5e)

![Screenshot from 2023-08-15 20-41-10](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/2c489024-2261-4972-9baa-8d33117c699f)


 
</details>

<details><summary><strong>Labs on "Incomplete overlapping Case"
</strong></summary>

## Example 1:

```
module incomp_case (input i0 , input i1 , input i2 , input [1:0] sel, output reg y);
	always @ (*)
	begin
	case(sel)
		2'b00 : y = i0;
		2'b01 : y = i1;
	endcase
	end
endmodule
```
## Simulation
![Screenshot from 2023-08-15 21-32-39](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/913dbab0-a435-4e1d-bd11-a5b1ace56ca9)


## Synthesis
![Screenshot from 2023-08-15 21-33-34](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/97f78006-4a8a-4179-aa1f-c2b66deef203)

![Screenshot from 2023-08-15 21-34-01](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/26eee149-2e0e-4f9c-b70d-ee6d70c795d0)


## Example 2:
```
module comp_case (input i0 , input i1 , input i2 , input [1:0] sel, output reg y);
always @ (*)
begin
	case(sel)
		2'b00 : y = i0;
		2'b01 : y = i1;
		default : y = i2;
	endcase
end
endmodule
```

## Simulation
![Screenshot from 2023-08-15 21-42-09](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/c781cf03-fbc0-4d4c-a279-bbacd3edb0d2)



## Synthesis

![Screenshot from 2023-08-15 21-36-46](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/c50b7ade-d910-4111-b0df-29972f4382c2)

![Screenshot from 2023-08-15 21-37-00](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/5ff993bf-b9e4-4379-be2e-e8aeb68b69c6)


## Example 3:
```
module partial_case_assign (input i0 , input i1 , input i2 , input [1:0] sel, output reg y , output reg x);
always @ (*)
begin
	case(sel)
		2'b00 : begin
			y = i0;
			x = i2;
			end
		2'b01 : y = i1;
		default : begin
	         	  x = i1;
			  y = i2;
		 	 end
	endcase
end
endmodule
```

## Simulation

![Screenshot from 2023-08-15 21-51-14](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/771ffa67-f694-409d-9bbe-c25037372d6d)


## Synthesis
![Screenshot from 2023-08-15 21-38-05](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/697dc64a-f0b1-4862-96aa-3844f74b1772)
![Screenshot from 2023-08-15 21-38-23](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/f15971a6-c60c-47d2-946e-c2a88182fcab)


## Example 4:
```
module bad_case (input i0 , input i1, input i2, input i3 , input [1:0] sel, output reg y);
always @(*)
begin
	case(sel)
		2'b00: y = i0;
		2'b01: y = i1;
		2'b10: y = i2;
		2'b1?: y = i3;
		//2'b11: y = i3;
	endcase
end
endmodule
```

## Simulation


![Screenshot from 2023-08-15 21-53-08](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/f26109b2-c0c8-4e84-9f69-874724b91aea)

## Synthesis

![Screenshot from 2023-08-15 21-39-13](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/a5084adb-d835-47c3-a85b-bec44c058fe3)

![Screenshot from 2023-08-15 21-39-39](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/503e4600-5f8a-4c0c-85dc-4cd9007a2010)

</details>
<details>
<summary><strong> For loop and for generate </strong></summary>

## For loop
Procedural 'for' loops are runtime evaluated as often as
neccesary when the procedural block is activated. They can be fully dynamic.
They MUST appear in a procedural block - thus have more limited use. 
It is used in "always" block.
It is used for evaluating expression multiple times.

## Syntax
```
for (<initiaization>, <condition>, <update>)begin
 \\ expression to be evaluated
end
```


## For generate
Generate loops are evaluated at compile / elaboration time. NOT
at runtime. So the loops limits must be fully "known" at elaboration time.
You're just about unlimited as to what can go inside a generate loop.
It is used outside the "always" block.
It is used for instantiating hardware multiple times.


## Syntax

```
genvar k;
generate 
    for (k = 0; k < 4; k++) begin
       \\ statements to be executed
       end
   end
endgenerate
```
 
</details>

<details><summary><strong>Labs on "for loop" and "for generate" 
</strong></summary>


## Example 1:

```
module mux_generate (input i0 , input i1, input i2 , input i3 , input [1:0] sel  , output reg y);
	wire [3:0] i_int;
	assign i_int = {i3,i2,i1,i0};
	integer k;
always @ (*)
	begin
	for(k = 0; k < 4; k=k+1) begin
		if(k == sel)
		y = i_int[k];
		end
	end
endmodule
```

## Simulation

![Screenshot from 2023-08-15 22-01-54](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/df4df0a6-1f4a-47c7-8b74-3e1c789cb73f)

## Synthesis

![Screenshot from 2023-08-15 22-12-37](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/e4239a9b-2ebe-40c2-a05b-644d63e10ec8)

## Netlist Simulation

![Screenshot from 2023-08-15 22-14-51](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/43cb35df-70cb-4ebe-b5d1-1b92f90f0e90)



## Example 2:

```
module demux_case (output o0 , output o1, output o2 , output o3, output o4, output o5, output o6 , output o7 , input [2:0] sel  , input i);
reg [7:0]y_int;
assign {o7,o6,o5,o4,o3,o2,o1,o0} = y_int;
integer k;
always @ (*)
begin
y_int = 8'b0;
case(sel)
	3'b000 : y_int[0] = i;
	3'b001 : y_int[1] = i;
	3'b010 : y_int[2] = i;
	3'b011 : y_int[3] = i;
	3'b100 : y_int[4] = i;
	3'b101 : y_int[5] = i;
	3'b110 : y_int[6] = i;
	3'b111 : y_int[7] = i;
endcase
end
endmodule

```

## Simulation
![Screenshot from 2023-08-15 22-03-25](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/e0c787eb-11d7-462e-9c54-72248f9070a1)


## Synthesis
![Screenshot from 2023-08-15 22-16-53](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/f246a734-2bcc-4bd1-89a6-30ef1280b90e)
![Screenshot from 2023-08-15 22-17-17](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/d1309118-1a35-4ec1-b1a2-66b21c8fbfb7)


## Netlist Simulation
![Screenshot from 2023-08-15 22-18-47](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/0913a91c-6b3b-4304-ada2-0a5a73bdc80b)


## Example 3:

```
module demux_generate (output o0 , output o1, output o2 , output o3, output o4, output o5, output o6 , output o7 , input [2:0] sel  , input i);
reg [7:0]y_int;
assign {o7,o6,o5,o4,o3,o2,o1,o0} = y_int;
integer k;
always @ (*)
begin
	y_int = 8'b0;
	for(k = 0; k < 8; k++) begin
		if(k == sel)
		y_int[k] = i;
	end
end
endmodule
```

## Simulation

![Screenshot from 2023-08-15 22-05-25](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/e0a00833-d257-418a-b46c-3277140c1ef9)

## Synthesis

![Screenshot from 2023-08-15 22-20-19](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/bb8537bf-6922-4902-ad7a-e1353cea9444)

## Netlist Simulation

![Screenshot from 2023-08-15 22-25-43](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/ce75e237-0b26-42a0-9ce4-e51abeb439a9)


## Example 4:

```
module rca (input [7:0] num1 , input [7:0] num2 , output [8:0] sum);
wire [7:0] int_sum;
wire [7:0]int_co;

genvar i;
generate
	for (i = 1 ; i < 8; i=i+1) begin
		fa u_fa_1 (.a(num1[i]),.b(num2[i]),.c(int_co[i-1]),.co(int_co[i]),.sum(int_sum[i]));
	end

endgenerate
fa u_fa_0 (.a(num1[0]),.b(num2[0]),.c(1'b0),.co(int_co[0]),.sum(int_sum[0]));


assign sum[7:0] = int_sum;
assign sum[8] = int_co[7];
endmodule

module fa (input a , input b , input c, output co , output sum);
assign {co,sum} =a+b+c;
endmodule
```

## Simulation
![Screenshot from 2023-08-15 22-09-14](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/aa509b57-cb55-41b3-94d9-23f1a4b53036)


## Synthesis
![Screenshot from 2023-08-15 22-22-18](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/ea006865-13ba-4d18-af0e-0f43c457fd1f)


## Netlist Simulation
![Screenshot from 2023-08-15 22-23-33](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/a0074f40-133c-4610-8acd-3696e5b8df09)

</details>

## References
1. https://yosyshq.net/yosys/
2. https://linux.die.net/man/1/iverilog
3. https://github.com/steveicarus/iverilog
4. https://gtkwave.sourceforge.net/gtkwave.pdf
5. https://ngspice.sourceforge.io/
6. http://opencircuitdesign.com/magic/
7. http://opensta.org/
8. https://openlane.readthedocs.io/en/latest/
9. https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop
