# Synapse
A Domain-Specific Language for Distributed Edge Computing

[![Version](https://img.shields.io/badge/version-0.1-brightgreen.svg)](https://pypi.org/project/ad-topic-recommender/)
[![License](https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-blue.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Python](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/downloads/)                                +

[//]: # ([![Build Status]&#40;https://travis-ci.com/dilshan/synapse.svg?branch=main&#41;]&#40;https://travis-ci.com/dilshan/synapse&#41;)

Synapse is a Domain-Specific Language (DSL) designed to simplify collaborative task execution on resource-constrained 
devices at the edge of the network.

## Project Overview

Traditional edge computing approaches rely on individual device capabilities. Synapse takes a different approach: 
it enables devices to work together, leveraging their combined processing power to handle complex tasks efficiently.

### This project aims to develop

- User-friendly DSL: Synapse provides a concise and intuitive way to define tasks suitable for distributed execution on 
edge devices.
- Secure Communication Protocol: This protocol ensures secure device discovery, task distribution, data exchange, and 
collaboration among participating devices.
- Scalable and Fault-Tolerant System: The paradigm can adapt to dynamic edge environments by handling device 
availability fluctuations and potential failures.

### Benefits

- Improved Processing Power: By leveraging collaboration, Synapse overcomes limitations of individual devices, enabling 
execution of complex tasks at the edge.
- Reduced Latency: Processing data closer to the source minimizes network hops, leading to lower latency for real-time 
edge applications.
- Scalability: The paradigm scales effortlessly as new devices join the network, automatically distributing workload 
without expensive upgrades.
- Simplified Development: The Synapse DSL simplifies task definition for developers, reducing the barrier to entry for 
edge computing projects.

## Development Stages 

### Core Modules

1. Synapse DSL:
    - Parser: Parses user-defined code written in the Synapse DSL.
    - Compiler: Generates optimized code for edge devices based on parsed DSL syntax.
    - Optimizer (Optional): Analyzes and optimizes the generated code for efficient execution on resource-constrained 
   devices.

2. Task Management:
    - Job Manager: Handles job creation, registration (with central server if used), and lifecycle management.
    - Task Decomposition: Breaks down the overall task into smaller, executable subtasks suitable for individual devices.
    - Result Aggregation: Collects and combines results from participating devices after task execution.
    - Leader Election: Implements logic for selecting a leader device to coordinate task execution and result aggregation.

### Communication Modules:

1. Device Discovery:
Implements the chosen mechanism for devices to find available tasks and collaborating participants (e.g., server-based 
discovery, peer-to-peer protocols).

2. Secure Communication:
    - Channel Establishment: Establishes secure communication channels between devices using encryption and 
   authentication protocols.
    - Data Exchange: Facilitates secure exchange of task details, code snippets, and results between devices.
    - Cryptography (Optional): Integrates chosen libraries (libsodium, NaCl) for encryption and decryption 
    functionalities.

### Security Module:

- Authentication and Authorization: Implements mechanisms for verifying device identities and access rights before 
allowing participation.
- Secure Key Management: Establishes secure methods for generating, storing, and rotating cryptographic keys used for 
encryption.

### Client Module:

- Job Management: Allows users to submit jobs, retrieve job details, and interact with task outcomes.
- Visualization Tools: Offers functionalities for visualizing results or task execution progress.

### Additional Considerations:

- Configuration Management: Utilize configuration files or environment variables to manage system parameters (e.g., 
server addresses, security keys) without modifying core code.
- Logging and Monitoring: Integrate logging mechanisms to track system events and enable monitoring for potential 
issues.

### Benefits of this Modular Structure:

- High Cohesion and Low Coupling: Modules are highly focused on specific functionalities and have minimal dependencies 
on each other, improving maintainability.
- Scalability and Reusability: Modules can be easily scaled or reused in future projects with similar requirements.
- Clear Separation of Concerns: Separates core task management logic from communication and security aspects, improving 
code clarity.
- Improved Testability: Modular design facilitates unit testing of individual modules and integration testing for 
communication between modules.

### Development Plan

1. Core System and Synapse DSL (Python):
	- Functionalities:
		- Job management (creation, registration, monitoring)
		- Client communication (sending/receiving tasks and results)
		- Synapse DSL parser
		- User interface (optional) for job submission and visualization
	- Language: Python
		Reason: Readability, simplicity, rich ecosystem of libraries for parsing (PLY, lark), networking (Twisted, asyncio) and UI development (Tkinter, PyQt).

2. Compiler (LLVM):
	- Functionalities:
		Generates optimized code for target edge device architectures from Synapse DSL code.
	- Language: LLVM
		Reason: Powerful compilation infrastructure for diverse architectures, potential for high performance.
	- Integration with Python:
		Use libraries like llvmlite to bridge Python and LLVM for code generation tasks within the Python core system.

3. Security (C/C++ or Go):

   - Functionalities:
       - Secure communication channel establishment (encryption, authentication)
       - Secure key management (generation, storage, rotation)
   - Language:
     - C/C++
       - Reason: Fine-grained control over memory and security aspects.
       - Integration: Separate codebase for security-critical functionalities. Utilize libraries like libsodium or NaCl.

4. Communication (Go or Python):
- Functionalities:
    - Device discovery (optional, depending on chosen mechanism)
    - Secure data exchange between devices
- Language:
Python with Libraries
Reason: Simpler development if communication needs are not complex.
Integration: Utilize libraries like Twisted or asyncio for asynchronous communication within the Python core system.

1. Testing and Deployment:

Develop unit tests for individual modules using frameworks like pytest (Python), Catch2 (C++), or testing (Go).
Integrate unit tests into your development workflow for continuous feedback.
Consider containerization (Docker) for packaging and deployment of your system components across different environments.

## Getting Started

This repository is currently under development.

# Future Improvements

Development of the Synapse DSL syntax and compiler.
Design and implementation of the secure communication protocol.
Exploration and integration of scalability and fault tolerance mechanisms.
Development of tools and libraries for efficient task execution on edge devices.
Contribution:
This project welcomes contributions from the developer community! Feel free to fork the repository, propose issues, or 
submit pull requests.

## License

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].
[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]  
[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa] 

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

## Contact Information

For questions or feedback, please contact the author:

- Author: Dilshan M. Karunarathne
- Email: ceo@altier.me
- Website: [http://altier.me](http://altier.me)
