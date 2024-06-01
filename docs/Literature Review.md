# A Distributed Programming Paradigm for Resource-Constrained Devices with the Introduction of a Domain-Specific Language

Research Work Proposal  
W. M. Dilshan Karunarathne  
EUSL/TC/IS/2019/COM/24  
19/COM/313  
Supervised By: Ms. K. Kethika  
Co-Supervised By: Ms. S. Disne  

Department of Computer Science  
Faculty of Applied  
Science Trincomalee Campus  
Eastern University of Sri Lanka  

## Tentative Title

A Distributed Programming Paradigm for Resource-Constrained Devices with the Introduction of a Domain-Specific Language

## Abstract 

This project proposes a novel distributed programming paradigm specifically designed for resource-constrained devices 
operating at the edge of the network. The paradigm leverages the combined processing power of nearby devices to tackle 
computationally intensive tasks, overcoming limitations of individual devices. A Domain-Specific Language (DSL) 
facilitates user-friendly task specification for collaborative execution, while secure communication protocols ensure 
reliable and efficient data exchange among participating devices. This research aims to develop a scalable and 
fault-tolerant solution for distributed task execution, enabling efficient processing at the edge with reduced latency.

## Introduction

The growing prevalence of edge computing brings data processing closer to data sources, enabling real-time applications 
with lower latency. However, individual edge devices often have limited processing power, memory, and storage.  
This project proposes a solution – a distributed programming paradigm that harnesses the collective power of multiple 
devices for collaborative task execution. By distributing tasks among nearby devices, the burden on any single device 
is reduced, leading to improved performance and enabling the execution of more complex tasks at the edge.

## Problem statement

Current approaches in edge computing primarily rely on the individual processing capabilities of each device. 
This poses limitations for applications requiring high computational power or real-time response. While some existing 
distributed computing paradigms exist, they may not be well-suited for the resource-constrained and dynamic nature of 
edge environments. This project addresses the need for a lightweight, secure, and scalable paradigm that empowers 
resource-constrained devices for collaborative processing at the edge.

## Methodology

This project will follow a research and development approach.
* Research Phase: A thorough review of existing literature on distributed computing paradigms and edge computing 
challenges will be conducted.
* Development Phase:
  * Domain-Specific Language (DSL): Design a user-friendly DSL to specify tasks suitable for parallel execution on 
  edge devices.
  * Secure Communication Protocol: Develop a secure communication protocol for device discovery, leader election 
  (sudoer selection), task distribution, progress monitoring, and secure data exchange.
  * Scalability and Fault Tolerance Mechanisms: Explore techniques to handle dynamic device availability, 
  network issues, and potential device failures. This might involve mechanisms for task migration, error handling, 
  * and self-healing.
