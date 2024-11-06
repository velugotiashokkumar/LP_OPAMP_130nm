
# Low Power Operational Amplifier in 130nm Technology

This project includes the simulation of two stage Operational Amplifier
design and postlayout simulation of different parameters of the Op-Amp.

# Contents
- [Overview of LV Op-Amp IP](##Overview-of-LV-Op-Amp-IP)
- [Block Diagram of Low Power Operational Amplifer IP](##Block-Diagram-of-Low-Power-Operational-Amplifer-IP)
- [Circuit Diagram of Low Power Operational Amplifer IP](##Circuit-Diagram-of-Low-Power-Operational-Amplifer-IP)
- [Specifications](##Specifications)
- [Performance Parameters](##Performance-Parameters)
- [Open Source Tools Used](#Open-Source-Tools-Used)
- [Installation in Ubuntu](#Installation-in-Ubuntu)
    - [eSim Installation](#eSim-Installation)
    - [Ngspice Installation](#Ngspice-Installation)
    - [SkyWater PDK Installation](#SkyWater-PDK-Installation)
    - [Magic Installation](#Magic-Installation)
- [Installation in Windows](#Installation-in-Windows)
    - [eSim Installation](#eSim-Installation)
- [Pre Layout Schematic and Simulations](#Pre-Layout-Schematic-and-Simulations)
- [Future Work](#Future-Work)
- [Author](#Author)
- [Acknowledgements](#Acknowledgements)


## Overview of LV Op-Amp IP
The low power operational amplifier consists of two stages and operates at 1.8V power. It is designed to meet a set of provided specification such as high gain and low power consumption.

This two-stage op-amp is designed using the Skywater 130nm technology library. The proposed two stage op-amp consists of NMOS current mirror as bias circuit, differential amplifier as the first stage and common source amplifier as the second stage. 

The first stage of an op-amp contributed high gain while the second stage contributes a moderate gain. The results show that the circuit is able to work at 1.8V power supply voltage (VDD)


## Block Diagram of Low Power Operational Amplifer IP

 <p align="center">
 <img width="800" height="500" src="/Images/N/block.png">
 </p>


## Circuit Diagram of Low Power Operational Amplifer IP

 <p align="center">
  <img width="800" height="500" src="/Images/N/circuit.png">
 </p>


## Specifications

<table align="center">
<tr>
    <th>Specification</th>
    <th>Value</th>
</tr>
<tr>
    <td>Differential Gain</td>
    <td>31.55dB</td>
</tr>
<tr>
    <td>CMRR</td>
    <td>41.4dB</td>
</tr>
<tr>
    <td>Gain Bandwidth Product</td>
    <td>46MHz</td>
</tr>
<tr>
    <td>Phase Margin</td>
    <td>101.93&deg;</td>
</tr>
<tr>
    <td>Input Offset Voltage</td>
    <td>-24.55mV</td>
</tr>
<tr>
    <td>Power Dissipation at <br/>
    60Hz 1mV p-p sinusoid <br/>
    with 1k&Omega;</td>
    <td>17&micro;W</td>
</tr>
<tr>
    <td>Slew Rate</td>
    <td>180 V/&micro;s</td>
</tr>
</table>


## Performance Parameters

| Parameter | Description | Min | Type | Max | Unit | Condition |
| :---:  | :-: | :-: | :-: | :---:  | :-: | :-: |
| Technology | 0.18 um CMOS Process | | | | | |
| VDD | Supply Voltage | 1.6 | 1.8 | 2.0 | V | T=-40C to 200C |
| CMRR | Common Mode Rejection Ratio | 1790 | 1750 | 1690 | - | T=-40C to 200C |
| V-offset | Output Offset Voltage | -1.77 | -0.85 | -0.38 | V | T=-40C to 200C |


# Open-Source-Tools-Used

- eSim 
    - eSim (previously known as Oscad / FreeEDA) is a free/libre and open source EDA tool for circuit design, simulation, analysis and PCB design. It is an integrated tool built using free/libre and open source software such as KiCad, Ngspice and GHDL. eSim is released under GPL.
    - https://esim.fossee.in/home

- Ngspice
    - ngspice is the open source spice simulator for electric and electronic circuits.
    - http://ngspice.sourceforge.net/

- SkyWater Open Source PDK
    - The SkyWater Open Source PDK is a collaboration between Google and SkyWater Technology Foundry to provide a fully open source Process Design Kit and related resources, which can be used to create manufacturable designs at SkyWater’s facility.
    - https://github.com/google/skywater-pdk

- Magic
    - Magic is a venerable VLSI layout tool, written in the 1980's at Berkeley by John Ousterhout, now famous primarily for writing the scripting interpreter language Tcl. Due largely in part to its liberal Berkeley open-source license, magic has remained popular with universities and small companies. The open-source license has allowed VLSI engineers with a bent toward programming to implement clever ideas and help magic stay abreast of fabrication technology.
    - http://opencircuitdesign.com/magic/

# Installation in Ubuntu
- The eSim Software is currently available for Windows 7, 8 and 10 and Ubuntu 16.04 LTS and above

- The Magic Design Tool is available for Ubuntu
- Ngspice is installed when eSim is installed, but if any other version is needed please follow the steps mentioned

- The Pre-requisites for installing the following in Ubuntu are
    - git 
    - make

- Install them using

    To make sure that you install the latest version of the software(that is the package information is up to date)
    ```
    $ sudo apt-get update
    ```

    ```
    $ sudo apt install git

    $ sudo apt install make
    ```

## eSim Installation
Please refer to the following links for proper installation of *eSim*
- https://static.fossee.in/esim/installation-files/Install_eSim_on_Windows.pdf

- https://github.com/FOSSEE/eSim/blob/master/INSTALL

## Ngspice Installation
Please refer to the following links for proper installation of *Ngspice*
- http://ngspice.sourceforge.net/download.html

## SkyWater PDK Installation
- In Windows
    - Download the GitHub Repository : https://github.com/google/skywater-pdk

- In Ubuntu
In terminal, execute the following commands

- To download the repository into the current working directory
    ```
    $ git clone git://opencircuitdesign.com/open_pdks
    ```

- Go to `open_pks` directory
    ```
    $ cd open_pdks
    ```

- Configure and install
    ```
    $ ./configure --enable-sky130-pdk

    $ make

    $ sudo make install
    ```

## Magic Installation
In terminal, execute the following commands

- To download the repository into the current working directory
    ```
    $ git clone git://opencircuitdesign.com/magic
    ```

- Go to `magic` directory

    ```
    $ cd magic
    ```

- Configure and install
    ```
    $ sudo ./configure

    $ sudo make

    $ sudo make install
    ```

# Installation in Windows
- The eSim Software is currently available for Windows 7, 8 and 10 and Ubuntu 16.04 LTS and above

- Ngspice and SkyWater PDK are installed when eSim is installed in Windows OS.

## eSim Installation
Please refer to the following links for proper installation of *eSim*
- https://static.fossee.in/esim/installation-files/Install_eSim_on_Windows.pdf
- https://static.fossee.in/esim/installation-files/eSim-2.3_installer.exe
