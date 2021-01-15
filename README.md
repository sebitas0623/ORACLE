# ORACLE

ORACLE: c**O**llabo**R**ation of d**A**ta and **C**ontrol p**L**an**E**s to detect DDoS attacks in a Software-Defined Networking (SDN) architecture. This DDoS detection system is composed by two modules: a control plane implementation developed in an **ONOS** controller, and a data plane implementation developed using the **P4**.  In order to communicate both planes is used the P4Runtime interface which allows controlling in real-time the data plane elements of a p4 device.

![](https://github.com/sebitas0623/ORACLE_ddos/blob/master/images/Archit.png)


## Getting Started

These instructions will guide you to run the detection mechanism under an ONOS+P4 experimental scenario. We recommend using an Ubuntu 18.04 virtual machine.

### Prerequisites

To run the DDoS detection system is needed to install at the virtual machine the following SDN controller:

- [ONOS (2.2.0 or greater)](https://wiki.onosproject.org/display/ONOS/Development+Environment+Setup "ONOS")

Builds and installs the following repositories needed for developing and testing P4 support in:

- [BMv2](https://github.com/p4lang/behavioral-model) (P4 software switch)
- [PI](https://github.com/p4lang/PI)
- [p4c](https://github.com/p4lang/p4c) (P4 compiler)

The best way to install the previus repositories is executing the tool that brings **ONOS**:

```
bash $ONOS_ROOT/tools/dev/p4vm/install-p4-tools.sh
```

##### Note:
It is possible that in the middle of the tool execution could appear the next issue: "sudo: pip2.7: command not found". The solution is to open the file ($ONOS_ROOT/tools/dev/p4vm/install-p4-tools.sh) and change all "pip2.7" by "pip". Then, run the file again.

## Prepering the TEST environment
- First, run the ONOS controller activating only the APPs required by the implementation. These applications are the bmv2-driver, gui, and the custom application in charge of the extraction of the flow information and the features calculation. Although, the last one mentioned is not installed yet into the ONOS, at the moment to be done it, the application is activivated automaticly. To run the ONOS controller, you must be located in **~/onos** directory. Then, execute the next command:  
```
ONOS_APPS=drivers.bmv2,gui,org.p4.template ok clean
```
- Then, download **ORACLE_ddos** repository into the home **(~/)** of you virtual machine.
- 

