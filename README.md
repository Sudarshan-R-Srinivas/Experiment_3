# Experiment-3: Design and Analysis of a MOS Differential Amplifier

## Aim
Design and Analyze the MOS differential amplifier circuit for the following specifcations and Perform DC analysis,Transient Analysis,Frequency response and extract parmeter.

## Given Specifications
- **Supply Voltage (VDD):** 2.2V  
- **Power Consumption (P):** ≤2mW  
- **Common Mode Input Voltage (Vicm):** 1.2V  
- **Common Mode Output Voltage (Vocm):** 1.25V  
- **Threshold Voltage (Vp):** 0.4V

## Given Circuit
![Differential Amplifier Circuit](https://github.com/Sudarshan-R-Srinivas/Experiment_3/blob/main/circuit.png?raw=true)

## Introduction to MOS Differential Amplifier
A MOS differential amplifier consists of two MOSFETs (M1 and M2) with their sources connected together. When different input voltages are applied to the gate terminals, the drain currents of M1 and M2 vary accordingly. However, when the same input voltage is applied, both transistors conduct equal currents. This configuration is known as a **common-mode input voltage differential amplifier**.

To ensure proper amplification characteristics, the MOSFETs must operate in the **saturation region** and not enter the **triode region**. The circuit’s performance is analyzed through **DC analysis, transient analysis, and AC analysis (frequency response).**

---

# Circuit-1: Differential Amplifier with Resistor Biasing
![With Resistor](https://github.com/user-attachments/assets/3ac01943-5bc4-4c2c-8b76-1e517bbf08ee)



## Required Components
- **MOSFETs:** M1, M2, M3  
- **Resistors:** Rss, Rd  
- **Voltage Sources:** VDD, Input signals(Vicm)  

## Design Procedure
1. Construct the circuit with MOSFETs M1 and M2 forming a differential pair.
2. Connect a resistor (Rss) at the common source terminal of M1 and M2 to define the bias current.
3. Compute the tail current (Iss) using the given power (P) and supply voltage (VDD).
4. Determine individual drain currents **Id1** and **Id2** under balanced conditions.
5. Select appropriate values for **Rss** and **Rd** to achieve the desired gain and output voltage swing.
6. Adjust the width (W) and length (L) of M1 and M2 to optimize performance.
   - **Calculated values:** **L = 190nm, W = 6.7877µm**

## DC Analysis
![DC Analysis](https://github.com/user-attachments/assets/109fba6d-d060-445c-a206-3046058ddc70)

- Select **DC operating point analysis** in the simulation setup.
- Run the simulation to obtain the drain current and output voltage values.
- Results confirm that **Vout** is as expected and **Id1 = Id2**, indicating balanced operation.

## Transient Analysis
![Transient Analysis](https://github.com/user-attachments/assets/1810d729-d02f-4c14-b9ca-e01a7df887ed)

- Set up **transient analysis** with a stop time of **5ms**.
- Observe the time-domain response of the amplifier.

## AC Analysis
- Perform **AC frequency response analysis** to determine gain and bandwidth.

---

# Circuit-2: Differential Amplifier with Current Source Biasing
![With Current Source](https://github.com/user-attachments/assets/34bd0217-289c-4d1e-ae91-00cdd0540c3d)


## Modification
- Replace the resistor **Rss** with a **current source (1mA)** to improve stability.

## DC Analysis
![DC Analysis](https://github.com/user-attachments/assets/370563f2-ed06-4b40-a74d-d160fba44b34)

- Run **DC operating point analysis** and verify bias stability.

## Transient Analysis
![Transient Analysis](https://github.com/user-attachments/assets/6a158a86-205b-47e3-a31e-0e8bde0ccc9f)

- Apply a **180-degree phase shift** to one MOSFET while keeping the other at **0 degrees**.
- Assign an **AC amplitude of 1** to one input and **0 to the other** (even -1).
- Run the simulation and analyze the improved transient response.

## AC Analysis
- Perform frequency response analysis to examine **gain and bandwidth**.

---

# Circuit-3: Differential Amplifier with MOSFET-Based Current Source
![With MOSFET-Based Current Source](https://github.com/user-attachments/assets/983385bf-3733-4fb4-a953-304fe54b38d5)


## Modification
- Replace the current source with a **MOSFET acting as an active current source**.
- Given parameters: **Vp = 0.4V, Vt = 0.36V**, leading to a **gate voltage of 0.76V**.
- Adjust **W/L ratio** of the new MOSFET to optimize performance.

## DC Analysis
![DC Analysis](https://github.com/user-attachments/assets/61bc8b8b-e8ea-4422-ab56-5af2c324f483)

- Execute **DC analysis** to verify effective tail current regulation.

## Transient Analysis
![Transient Analysis](https://github.com/user-attachments/assets/14d76795-ddc9-4edc-8de4-910a5d05be19)

- Apply an **AC amplitude of 1** to one MOSFET and **0 to the other**.
- Run the simulation to observe improved transient response.

## AC Analysis
- Analyze **gain and bandwidth performance**.

## DC Sweep Analysis
- Conduct a **DC sweep** to examine output variations across a range of input conditions.

---

# Results

## Circuit-1 (Resistor-Based Design)
- DC analysis confirms **MOSFET operation in saturation** with equal drain currents for identical inputs.  
- Transient response demonstrates **proper differential operation**.  
- AC analysis reveals **moderate gain and limited common-mode rejection**.  

## Circuit-2 (Current Source Biasing)
- Replacing the resistor with a **current source** improves **bias stability**.  
- The transient response is **more stable and symmetrical**.  
- AC analysis shows **higher gain and increased bandwidth** compared to Circuit-1.  

## Circuit-3 (MOSFET-Based Current Source)
- DC analysis validates that the **MOSFET-based current source effectively regulates tail current**.  
- Transient response is **more accurate and stable**.  
- AC analysis demonstrates **higher gain and improved frequency response**.  
- DC sweep confirms the expected **output variations based on input changes**.  

---

# Inference
- The **tail current source** significantly impacts the amplifier’s **gain and stability**.  
- The **resistor-based design** has **lower gain and poor common-mode rejection**.  
- A **current source bias** enhances **stability and differential operation**.  
- A **MOSFET-based current source** provides the **best gain, stability, and frequency response**, making it the most efficient configuration.  

