# Tutorial 9: Developing Industrial Strength EDA Tools Using the OpenDB Open-source Database and the OpenROAD Framework

This repository contains all material needed to participate in the live tutorial of OpenROAD at DAC 2020. Star or bookmark this repository for future reference.

## Live Session Details

**Date:** Monday July 20, 2020.

**Tutorial Link** 
* [Part 1](http://www2.dac.com/events/eventdetails.aspx?id=295-228) at 1:30 PM PT. [Convert to your timezone](https://www.timeanddate.com/worldclock/converter.html?iso=20200720T203000&p1=224&p2=75&p3=70&p4=179&p5=136&p6=37&p7=195&p8=438&p9=33&p10=241&p11=240)
* [Part 2](http://www2.dac.com/events/eventdetails.aspx?id=295-235) at 4:00 PM PT. [Convert to your timezone](https://www.timeanddate.com/worldclock/converter.html?iso=20200720T230000&p1=224&p2=75&p3=70&p4=179&p5=136&p6=37&p7=195&p8=438&p9=33&p10=241&p11=240)

**How to join**

The live session requires registration to the DAC conference. 

To join the session, login to the virtual event platform for DAC, navigate to the agenda and select Monday 1:30PM. Click on the session and join the live meeting. Instructions for signing in to the platform is sent to registrants on the email.

## Getting Help

If you have any questions before, during or after the tutorial, feel free to email [ahosny@openroad.tools](mailto:ahosny@openroad.tools)

## Prepare Your Environment

During the tutorial, we will be covering how to get started with OpenROAD. However, that’s not all. We will be presenting how to develop tools using OpenROAD infrastructure, and how to contribute to its master codebase. For full participation in the tutorial, we ask you to prepare your machine as detailed below.

### Supported Platforms
* CentOS 7: https://www.centos.org/download/
* Ubuntu 18: https://releases.ubuntu.com/18.04/
* Windows 10 using WSL: https://ubuntu.com/wsl

If you are not using any of the two platforms, we suggest that you download VirtualBox (https://www.virtualbox.org/) and install a supported platform. Alternatively, you can install Docker (https://docs.docker.com/get-docker/) and pull an official image.

### Prerequisites
OpenROAD tools only need `Tcl` to be installed.
* CentOS: `sudo yum install tcl`
* Ubuntu: `sudo apt install tcl`

To use the full automation features of OpenROAD flow, you need to install:
* `Python 3`
    * CentOS: `sudo yum install python3`
    * Ubuntu: `sudo apt install python3`
* Time
    * CentOS: `sudo yum install time`
    * Ubuntu: `sudo apt install time`
* KLayout
Follow instructions here: https://www.klayout.de/build.html

### Download OpenROAD Tools
Download pre-built tools from: https://github.com/The-OpenROAD-Project/OpenROAD/releases
After you download, extract the downloaded file and add it to the PATH environment variable using: `export PATH=</path/to/openroad/bin>:</path/to/openroad>:$PATH`

### Test OpenROAD Tools
From the terminal screen, type in:
```shell
$ openroad
| OpenROAD 0.9.0 bfb1291039
| This program is licensed under the BSD-3 license. See the LICENSE file for details. 
| Components of the program may be licensed under more restrictive licenses which must be
| honored.
%
```

If you see the above OpenROAD message, that means tools are working properly.

### Development Dependencies
If you are planning to dive into OpenROAD data models using C++, you will need to install development dependencies to be able to build the tool from sources.

Development dependencies are documented in this Dockerfile: https://github.com/The-OpenROAD-Project/OpenROAD/blob/master/Dockerfile

## Tutorials

1. [Let's verify your installation](1_verify_installation)
2. [Database access, features and tools](2_database_access)
3. [RTL to GDS autonomous flow](3_rtl_to_gds_autonomous_flow)
4. [Generating reports](4_generating_reports)
5. [Antenna fix example](5_antenna_fix_example)
6. [Layout Visualization](6_layout_visualization)
7. [OpenDB Python API](7_opendb_python_api)
8. [Machine learning example](8_machine_learning_example)
9. [Adding a tool to OpenROAD](9_adding_a_tool_example)


## OpenROAD Cloud

You can run OpenROAD flow without installing the tools locally by using OpenROAD public cloud service.

OpenROAD Cloud is available at https://cloud.theopenroadproject.org/

At the time of the tutorial, the platform offers OpenROAD flow on Nangate45. Support for Skywater PDK is in progress.

## Citations

If you are using example codes from this repository in your research, we appreciate your citation to the following articles:

```JavaScript
@inproceedings{9105619,  
    author={A. {Hosny} and A. B. {Kahng}},  
    booktitle={2020 33rd International Conference on VLSI Design and 2020 19th International Conference on Embedded Systems (VLSID)},   
    title={Tutorial: Open-Source EDA and Machine Learning for IC Design: A Live Update},   
    year={2020},  
    volume={},  
    number={},  
    pages={1-14}
}

@inproceedings{10.1145/3316781.3326334,
    author = {Ajayi, Tutu and Chhabria, Vidya A. and Foga\c{c}a, Mateus and Hashemi, Soheil and Hosny, Abdelrahman and Kahng, Andrew B. and Kim, Minsoo and Lee, Jeongsup and Mallappa, Uday and Neseem, Marina and Pradipta, Geraldo and Reda, Sherief and Saligane, Mehdi and Sapatnekar, Sachin S. and Sechen, Carl and Shalan, Mohamed and Swartz, William and Wang, Lutong and Wang, Zhehong and Woo, Mingyu and Xu, Bangqi},
    title = {Toward an Open-Source Digital Flow: First Learnings from the OpenROAD Project},
    year = {2019},
    isbn = {9781450367257},
    publisher = {Association for Computing Machinery},
    address = {New York, NY, USA},
    url = {https://doi.org/10.1145/3316781.3326334},
    doi = {10.1145/3316781.3326334},
    booktitle = {Proceedings of the 56th Annual Design Automation Conference 2019},
    articleno = {76},
    numpages = {4},
    location = {Las Vegas, NV, USA},
    series = {DAC ’19}
}
  

```

## License
BSD 3-Clause License. See [LICENSE](LICENSE) file.
