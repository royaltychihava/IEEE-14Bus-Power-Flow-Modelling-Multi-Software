# IEEE 14-Bus Power System Modelling and Validation (Multi-Software)

## Overview
This project presents the modelling and power flow analysis of the IEEE 14-bus test system across three software environments:

- PowerWorld Simulator  
- DIgSILENT PowerFactory  
- MATLAB Simulink  

The results from each platform are compared with benchmark system data to evaluate accuracy and modelling consistency.

---

## Objective
- Model the IEEE 14-bus system in multiple simulation environments  
- Perform power flow analysis using each platform  
- Validate simulation results against known system data  
- Compare modelling accuracy across tools  

---

## Reference System

### IEEE 14-Bus Network
![Network](ieee14bus_actual_network.png)

Standard IEEE 14-bus system used as the reference model.

---

### Branch Data
![Branch Data](ieee14bus_branch_data.png)

Defines transmission line parameters and system topology.

---

### Benchmark System Results
![Actual Results](ieee14bus_actual_results.png)

Reference results used to validate all simulations.

---

## PowerWorld Simulation

### Model Implementation
![PowerWorld Model](powerworld_model.png)

- Network recreated using PowerWorld Simulator  
- Includes buses, generators, loads, and transformers  
- Newton-Raphson power flow used  

---

### Simulation Results
![PowerWorld Results](powerworld_results.png)

- Voltage magnitudes match within **0.007 pu**  
- Voltage angles match within **0.1°**  

✔ Results closely align with benchmark data  
✔ Minor differences due to modelling approximations  

---

## DIgSILENT PowerFactory Simulation

### Model Implementation
![PowerFactory Model](powerfactory_model.png)

- System modelled using PowerFactory components  
- Includes detailed representation of:
  - Lines  
  - Transformers  
  - Loads  
  - Generators  

---

### Simulation Results
![PowerFactory Results](powerfactory_results.png)

- Voltage magnitude error ≤ **0.001 pu**  
- Voltage angle error ≤ **0.04°**  

✔ Highest accuracy among the three platforms  
✔ Validates PowerFactory’s modelling precision  

---

## MATLAB Simulink Simulation

### Model Implementation
![Simulink Model](simulink_model.png)

- Built using Simulink power system components:
  - Three-phase sources  
  - RLC branches  
  - Transformers  
  - Measurement blocks  

---

### Simulation Results
![Simulink Results](simulink_results.png)

- Voltage magnitude error ≤ **0.017 pu**  
- Voltage angle error ≤ **0.592°**  

✔ Results closely match benchmark values  
✔ Slightly larger deviations due to modelling approximations  

---

## Comparison of Results

| Software        | Voltage Error (pu) | Angle Error (°) |
|----------------|------------------|----------------|
| PowerWorld     | ≤ 0.007          | ≤ 0.1          |
| PowerFactory   | ≤ 0.001          | ≤ 0.04         |
| Simulink       | ≤ 0.017          | ≤ 0.592        |

---

## Key Insights

- All three platforms successfully replicate the IEEE 14-bus system  
- PowerFactory provides the highest accuracy  
- PowerWorld offers efficient and intuitive modeling  
- Simulink provides flexibility for dynamic and control-based simulations  
- Differences arise due to:
  - Modelling assumptions  
  - Numerical methods  
  - Component approximations  

---

## Tools Used

- PowerWorld Simulator  
- DIgSILENT PowerFactory  
- MATLAB Simulink  

---

## Files

- PowerWorld_IEEE14Bus_Model_and_Report.zip  
- PowerFactory_IEEE14Bus_Model_and_Report.zip  
- Simulink_IEEE14Bus_Model_and_Report.zip  

---

## Conclusion

This project demonstrates that multiple simulation platforms can accurately model and analyze power systems. While minor discrepancies exist, all tools provide reliable results. The comparison highlights the strengths of each platform and validates their use for power flow studies and system analysis.

---

## Author

Royalty Holyworth Chihava
