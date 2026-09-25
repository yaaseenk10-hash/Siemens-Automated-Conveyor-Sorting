# Siemens Automated Conveyor Sorting System

## Overview

This project is a simulated automated conveyor sorting system developed using Siemens TIA Portal. It combines S7-1500 ladder logic with an HMI to control and monitor a conveyor, sorting diverter, sensors, production counters, and fault conditions.

The project was created to develop practical experience with PLC programming, HMI design, industrial control sequences, alarms, and system troubleshooting.

## Main Features

- Automatic and manual operating modes
- Start, stop, and reset controls
- Simulated entry, reject, and exit sensors
- Automatic and manual diverter control
- Accepted and rejected part counters
- Conveyor motor and system-running indicators
- Diverter-active indicator
- Conveyor jam detection
- Latched jam fault with reset logic
- HMI discrete alarm for conveyor jams
- Safety status simulation and control interlocks

## Software and Equipment

- Siemens TIA Portal Cloud V21
- Siemens S7-1500 CPU 1511-1 PN
- SIMATIC KTP700 Basic PN HMI
- WinCC HMI
- S7-PLCSIM Advanced
- Ladder Logic

## Control Sequence

1. The system is enabled when the safety condition is healthy.
2. Pressing **Start** activates the system and conveyor.
3. The entry sensor detects a part entering the conveyor.
4. A rejected part activates the sorting request and diverter.
5. The exit sensor completes the sorting sequence and resets the diverter request.
6. Accepted and rejected parts are recorded by separate counters.
7. If a part remains detected too long, the system generates and latches a jam fault.
8. The jam fault stops the conveyor and activates the HMI alarm.
9. After the obstruction is cleared, the operator can reset the system.

## HMI Functions

The HMI allows the operator to:

- Start and stop the conveyor
- Reset the control sequence
- Select automatic mode
- Simulate safety and sensor signals
- Operate the conveyor and diverter manually
- Monitor system, motor, diverter, and fault status
- View and reset production counters
- View conveyor jam alarms

## Testing

Testing included:

- Normal start and stop operation
- Automatic and manual control
- Accepted and rejected part sequences
- Diverter activation and reset
- Production counter operation
- Jam detection and fault latching
- Alarm triggering
- Fault and counter reset behavior

## Screenshots

Screenshots of the HMI, ladder logic, alarm system, and simulation testing will be included in the repository.

## Demo

A short demonstration video showing the system operating in simulation will be added here.

## Project Status

The PLC program and HMI are complete and have been tested successfully in simulation.

> **Note:** This project was developed and tested entirely through simulation. It was not connected to physical conveyor hardware or a safety-rated emergency-stop circuit.
