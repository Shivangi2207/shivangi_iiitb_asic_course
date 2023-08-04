# Shivangi_iiitb_asic_course
## Table of Contents
-[Day 0](#day-0)

-[References](#references)

-[Day 1](#day-1)



## Day 0


<details>
  <summary><strong>Yosys</strong></summary>

  ## What is yosys?
  
  Yosys is a framework for Verilog RTL synthesis.
  It currently has extensive Verilog-2005 support and provides a basic set of synthesis algorithms for various application domains. 
  Yosys can be adapted to perform any synthesis job by combining the existing passes (algorithms) using synthesis scripts and adding    additional passes as needed by extending the Yosys C++ code base.
  Yosys is free software licensed under the ISC license (a GPL compatible license that is similar in terms to the MIT license or the 
  2-clause BSD license).



## Commands to install Yosys(for linux)

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

<details>
  <summary><strong> Icarus verilog</strong></summary>

## What is iverilog?

Icarus verilog is a compiler that translates Verilog source code into executable programs for simulation, or other netlist formats for further processing. The currently supported targets are vvp for simulation, and fpga for synthesis. 


## Commands to install iverilog

```

sudo apt-get install iverilog
```

![Screenshot from 2023-07-31 09-59-32](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/6338283f-7296-4109-8ccb-638488b8c950)

</details>

<details>
  <summary><strong>Gtkwave</strong></summary>

## What is GTKWave?

GTKWave is an analysis tool used to perform debugging on Verilog or VHDL
simulation models. With the exception of interactive VCD viewing, it is not
intended to be run interactively with simulation, but instead relies on a post-
mortem approach through the use of dumpfiles. 

  ## Commands to install gtkwave




```
sudo apt update

sudo apt install gtkwave
```
![Screenshot from 2023-07-31 10-00-10](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/5d015986-fa7c-4114-ab27-71e5090eb0b5)
</details>

<details>
<summary><strong>Ngspice</strong></summary>
 
  ## What is Ngspice?
 Ngspice is the open source spice simulator for electric and electronic circuits.
 Ngspice offers a wealth of device models for active, passive, analog, and digital elements. Model parameters are provided by our       collections, by the semiconductor device manufacturers, or from semiconductor foundries. The user adds her circuits as a netlist, and the output is one or more graphs of currents, voltages and other electrical quantities or is saved in a data file.

  
  ## Installation of Ngspice
Download the tarball from https://sourceforge.net/projects/ngspice/files/ to a local directory and then follow the commands given below :
## Dependency for Ngspice:

```
sudo apt-get install libxaw7-dev
```

## Commands for installation:

```
tar -zxvf ngspice-40.tar.gz
cd ngspice-40
mkdir release
cd release
../configure  --with-x --with-readline=yes --disable-debug
make
sudo make install
```

![Screenshot from 2023-08-02 11-50-49](https://github.com/Shivangi2207/shivangi_iiitb_asic_course/assets/140998647/8f533196-cc13-4d60-bb26-73b644097f62)

  
</details>

<details>
<summary><strong>Magic</strong></summary>
 
  ## What is Magic?
  
  Magic is a venerable VLSI layout tool, written in the 1980's at Berkeley by John Ousterhout, now famous primarily for writing the scripting interpreter language Tcl. Due largely in part to its liberal Berkeley open-source license, magic has remained popular with universities and small companies. The open-source license has allowed VLSI engineers with a bent toward programming to implement clever ideas and help magic stay abreast of fabrication technology. However, it is the well thought-out core algorithms which lend to magic the greatest part of its popularity. Magic is widely cited as being the easiest tool to use for circuit layout, even for people who ultimately rely on commercial tools for their product design flow. 

  ## Commands to install Magic

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

<details>
<summary><strong>OpenSTA</strong></summary>

## What is OpenSTA?
OpenSTA is a distributed software testing architecture designed around CORBA, it was originally developed to be commercial software by CYRANO. The current toolset has the capability of performing scripted HTTP and HTTPS heavy load tests with performance measurements from Win32 platforms. However, the architectural design means it could be capable of much more.

## Commands to install OpenSTA

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

<details>
<summary><strong>OpenLANE</strong></strong></summary>

## What is OpenLANE?

OpenLane is an automated RTL to GDSII flow based on several components including OpenROAD, Yosys, Magic, Netgen, CVC, SPEF-Extractor, KLayout and a number of custom scripts for design exploration and optimization. It also provides a number of custom scripts for design exploration and optimization.
OpenLane abstracts the underlying open source utilities, and allows users to configure all their behavior with just a single configuration file.

## Installation of OpenLANE

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

<details>
<summary>day1</summary>
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
