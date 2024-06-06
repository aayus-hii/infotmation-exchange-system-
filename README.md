# infotmation-exchange-system-
Project Overview
This project revolves around creating a system that allows the exchange of information between three distinct programs written in C++ and Python, leveraging a custom REST API. The primary objective is to develop scripts that generate, fetch, and display data in a synchronized manner.

Scripts and Their Functions

Script A (C++)
Core Features:
Executes a counter that increments by 0.1 units in each loop cycle.
Captures and prints the latest timestamp at the end of every iteration.
Shares counter values and timestamps at the loop's conclusion.
Operates at a frequency of 100Hz.

Script B (C++)
Core Features:
Retrieves shared values from Script A during each loop iteration.
Stores and displays the fetched values appropriately.
Acts as a host for an API facilitating external data exchanges.
Runs at a frequency of 200Hz.

Script C (Python)
Core Features:
Collects data from Script B through API calls.
Presents the fetched values in an organized manner.
Operates at a frequency of 10Hz.

Project Objective

The primary goal is for Script B to acquire values from Script A and showcase them on the console. Additionally, Script C should obtain data from Script B via REST API calls and display them as well.

Setup and Execution Guide

Requirements:
A C++ compiler (e.g., g++) for compiling Scripts A and B.
Python 3.x installed for running Script C.
Essential libraries such as cpprestsdk for Script B and the requests library for Script C (pip install requests).
Compilation and Execution:

Compile and execute Script A:
g++ -std=c++11 script_A.cpp -o script_A
./script_A

Compile and execute Script B:
g++ -std=c++11 script_B.cpp -o script_B -lcpprest -lssl -lcrypto -lboost_system
./script_B

Run Script C using Python:
python3 script_C.py

