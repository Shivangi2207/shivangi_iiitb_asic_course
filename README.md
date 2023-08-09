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
