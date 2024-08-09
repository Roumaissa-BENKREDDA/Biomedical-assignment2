# Biomedical-assignment3
<div align="center">
  <a href="https://unige.it/en/">
    <img src="./logounige.jpg" width="20%" height="20%" title="University of Genoa" alt="University of Genoa">
  </a>
</div>

<h1 align="center"> Phantom Omni Control Using PhanTorque Libraries </h1>

> **Authors:**
> - *Roumaissa Benkredda*  
> - *Karim Triki*  
> - *Ines Haouala*  
>
> **Professor:**
> - *Maura Casadio*
>
> **Submission Date:** February 9,2024


---

<a name="introduction"></a>

## Introduction

This repository contains materials related to the use of the Phantom Omni device in a biomedical robotics assignment. The project focuses on designing a reaching task and a controller for a planar manipulator using different force fields. The Phantom Omni device is controlled using the PhanTorque libraries in MATLAB/Simulink, which facilitate the implementation of control algorithms.

---

<a name="phantom-omni-overview"></a>

## Phantom Omni Overview

The Phantom Omni is a 3D haptic device used to interact with virtual environments through tactile feedback. It allows precise control of the end effector in a 3D space and can simulate various physical interactions, making it an excellent tool for research and development in fields like robotics and biomedical engineering.

![Phantom Omni](./2omni.png)

---

<a name="phantorque-libraries"></a>

## PhanTorque Libraries

The PhanTorque libraries are designed to interface the Phantom Omni and other Sensable haptic devices with MATLAB/Simulink, allowing for advanced control and simulation tasks.

<a name="3dof-library"></a>

### 3Dof Library

The 3Dof library is specifically tailored for the Phantom Omni and Phantom Desktop devices. It includes blocks for calculating the Jacobian and controlling the device in a 3D space. 

Key blocks include:
- **Omni Jacobian**: Computes the Jacobian matrix for the device.
- **Omni Jacobian Transpose**: Computes the transpose of the Jacobian matrix for control purposes.

<a name="6dof-library"></a>

### 6Dof Library

The 6Dof library is designed for use with the Phantom Premiums 1.5 device, allowing for full 6 degrees of freedom (DoF) control. This library includes additional features for torque control and advanced kinematic calculations.

---

<a name="reaching-task-and-force-fields"></a>

## Reaching Task and Force Fields

The project includes a task where the Phantom Omni is used to control a cursor in a virtual environment to reach multiple target points. The force fields applied by the device are based on its position and velocity, simulating physical interactions such as attraction to a target and resistance to motion (viscous field).

### Task Details:
- **Reaching Task**: The cursor must reach eight targets arranged in a circle, starting from a central target.
- **Force Fields**: Includes an attractive field towards the target and a viscous field opposing the cursor's velocity.

---

<a name="installation-instructions"></a>

## Installation Instructions

To use the PhanTorque libraries with MATLAB/Simulink:

1. **Unzip the Library Files**: Unzip the PhanTorque 3Dof or 6Dof library files.
2. **Add the Libraries to MATLAB Path**: Place the unzipped folder in your MATLAB directory and add it to the MATLAB path.
3. **Compile the S-Functions**:
   - Open MATLAB and navigate to the directory containing the S-function files.
   - Use the `mex` command to compile the functions. For example:
     ```matlab
     mex PhanTorque3Dof.c hd.lib hdu.lib
     ```
   - Ensure the OpenHaptics libraries are correctly linked in your `mexopts.bat` file.

4. **Run the Simulink Model**: Load the Simulink model provided and start the simulation to see the Phantom Omni in action.

---

<a name="references"></a>


