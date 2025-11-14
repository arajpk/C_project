
# Smart Energy Monitoring & Control System

The Smart Energy Monitoring & Control System is a C-based simulation designed to model household appliances and their energy usage.
The system uses simulated sensor inputs (presence, light intensity, and temperature) to automate appliance control and measure total energy consumption, running time, and activity history.
This project serves as a practical demonstration for embedded systems, automation logic, and energy-efficiency analysis.


## Key Features

- ## Appliance Monitoring:
Tracks the ON/OFF status, power rating, energy consumed (Wh), total ON duration, and last active timestamp for each appliance.

- ## Automation Based on Sensor Inputs:

Light control using presence and light intensity

Fan control using presence and temperature threshold

AC control based on high temperature

Fridge remains constantly ON to simulate real-world behavior

- ## Event Logging:
Maintains a list of all ON/OFF actions, each recorded with a timestamp.

- ## Manual Override:
Allows user-controlled toggling of selected appliances such as the TV and Washing Machine.

- ## Menu-Driven Interface:
Provides a clear, step-by-step simulation environment.


## Workflow Overview

- Appliances are initialized with predefined ratings and default states.

- User selects either random sensor simulation or manual sensor input.

- Automation logic updates appliance states based on sensor values.

- Energy usage and ON-time are calculated continuously.

- All state changes are logged.

- Users can view status, check energy totals, review logs, or toggle appliances manually.

- A final summary is shown when the user exits the simulation.



## Requirements and Setup
## System Requirements

- GCC or any standard C compiler

- Standard C libraries (time.h, stdio.h, stdlib.h, string.h)

- Terminal or command prompt for execution

- Recommended Project Structure

## C_project/ 
- ## include/
appliance.h
log.h
utils.h

- ## src/
appliance.c
log.c
utils.c
main.c

- Jenkinsfile
- Makefile

- README.md

## Setup

- Store header files inside the include/ directory.

- Store source files inside the src/ directory.

- Compile using either the Makefile or a standard GCC command.

- Run the resulting executable through the terminal.
## Usage and Results

## How to Use the Application

- Select sensor mode: random simulation or manual input.

- Observe how the system automatically controls appliances.

- Access appliance status to view:

1) ON/OFF state

2) Power consumption

3) Total running time

4) Energy consumed

5) Last activity timestamp

- Review the event log for recent updates.

- Manually toggle appliances when required.

- Exit to receive a final summary of total energy consumed and total simulated time.

## Expected Results

- Accurate and incremental tracking of ON duration.

- Realistic calculation of energy usage in Wh and kWh.

- Comprehensive event logs showing all state transitions.

- Clear and concise summary at the end of simulation
## CI/CD Pipeline (Jenkins)

## Purpose

The pipeline automates compiling, running, and archiving the project to ensure consistent builds and easy deployment.

- Pipeline Stages


1) Build: Cleans old outputs and compiles the project using the Makefile.


2) Run: Executes the built application to verify correct operation.


3) Archive: Stores the final executable as an artifact.


- Post-Build Actions


1) Shows a success message if the pipeline completes properly.


2) Displays an error message if any stage fails.

