## Shivangi_iiitb_asic_course

## TAPEOUT PROCESS
 This github repository summarizes the process required  during tapeout.

## Quick links:

[Day 0](#day-0)

[Day 1](#day-1)


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
<details>
	<summary><strong>Optimisation logic techniques</strong></summary><br>
	Logic optimization is a process of finding an equivalent representation of the specified logic circuit under one or more specified constraints. This process is a part of a logic synthesis          applied in digital electronics and integrated circuit design. 
	There are two types of optimisation logic
	<details><summary><strong>1. Combinational logic optimisation</strong></summary><br>
 	In this the logic gates get squeezed  to get the most optimized design that results in area and power saving.
  It is done by two means:
  1. constant propagation logic optimisation
  Constant Propagation is an optimization technique employed by synthesis tools to minimize hardware implementation. This is achieved by optimizing away the logic for which parameters are configured to keep it disabled.

let's understand it by an example:

In this example we fixed one of our input A to 0 then progate it to the output. So we can simply replace the whole big circuit with just and inverter as both are having same output.

![IMG_20230815_131136](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/f21a189f-ccb8-4959-99a9-406fd5a07898)

2.Boolean logic optimisation
The optimization methods that consider logic functions as well as their representations are called "Boolean methods"
Boolean function minimizing methods include: 
 a. Karnaugh maps
 b. Quine–McCluskey algorithm

 let's understand it by an example:
 In this optimisation we basically try to reduce the boolean expression using required methods.Hence we get the reduced logic expression 
 
![IMG_20230815_131122](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/7298588e-8a12-4a10-838b-2085b225d765)

	
 </details>
<details>
<summary><strong>Sequential logic optimisation</strong></summary>
sequential logic optimization method has been presented that is based on selectively precomputing the output logic values of the circuit one clock cycle before they are required, and using the precomputed values to reduce internal switching activity in the succeeding clock cycle
It is done by various means:
1. sequential constant propagation
Let's understand this using an example

![IMG_20230815_145417](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/191cb347-68d8-432e-bab3-9316295bb3b4)

In the 1st Dff Q will always be 0 when reset is high Q become 0 also when reset is not high it will be 0 again as D is grounded . So Q=0 is propagated to nand gate so our output will always be 1. But this is not the case with the 2nd Dff as in this Q=1 when set is high and Q=0 when set is not applied and D is grounded.

So in the 1st Dff Q pin is constant so it can be optimised furthur , but  the 2nd Dff can't be optimised as its Q pin is not constant.

2. State optimisation
In this optimisation of unused states are done.

3. Cloning
4. 

 
</details>

 
</details>
<details>
<summary><strong>Combinational logic optimisation lab work</strong></summary>

## code of file 
 
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
