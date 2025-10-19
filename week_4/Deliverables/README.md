# Week 4 Task – CMOS Circuit Design (sky130-style)

## Introduction

This lab explores CMOS circuit design using the **Sky130 PDK** through a sequence of SPICE simulations.  
It demonstrates how transistor-level device properties influence timing behavior analyzed in Static Timing Analysis (STA).  
By observing current-voltage characteristics, threshold extraction, inverter transfer characteristics, transient delays, noise margins, and variations, we gain a practical understanding of how real circuits behave under different conditions.

---

## 1. MOSFET Behavior & Id vs. Vds Characteristics

### Objective
To simulate the NMOS device and study how drain current (Id) varies with drain voltage (Vds) for different gate voltages (Vgs), identifying linear and saturation regions.

### Description
A SPICE simulation of NMOS (tt model) was carried out following the workshop steps.

### Result
![First_Spice_Simulation](/week_4/Deliverables/SPICE_Lab_with_sky130_models/First_Spice_Simulation.png)

**Observation:**  
As Vds increases, Id initially grows linearly (ohmic region) and then saturates beyond a certain Vds, showing channel pinch-off.  
This demonstrates the transition between triode and saturation regions.

---

## 2. Threshold Voltage Extraction & Velocity Saturation

### Objective
To sweep Vgs vs. Id and extract the device threshold voltage (Vt), and observe velocity saturation effects.

### Description
The Id–Vgs characteristics were simulated for constant Vds. The threshold voltage was extracted via linear extrapolation in the subthreshold region.

### Result
![Labs_Sky130_Id_Vds](/week_4/Deliverables/Labs_Sky130_Id_Vgs/Labs_Sky130_Id_Vds.png)
![Labs_Sky130_Id_Vgs](/week_4/Deliverables/Labs_Sky130_Id_Vgs/Labs_Sky130_Id_Vgs.png)
![Labs_Sky130_Vt](/week_4/Deliverables/Labs_Sky130_Vt/Labs_Sky130_Vt.png)

**Observation:**  
Vt is determined from the x-axis intercept of the tangent drawn to the linear region.  
Velocity saturation becomes prominent in short-channel devices, limiting current growth with increasing Vds.

---

## 3. CMOS Inverter: Voltage Transfer Characteristic (VTC)

### Objective
To build and simulate a CMOS inverter and plot its Voltage Transfer Characteristic (VTC).

### Description
A CMOS inverter (PMOS + NMOS) was constructed and simulated to obtain Vout vs. Vin curve.

### Result
![plot_vin_vs_vout_with_switching_threshold](/week_4/Deliverables/day_3/Labs_Sky130_SPICE_Simulation_for_CMOS/plot_vin_vs_vout_with_switching_threshold.png)

**Switching Threshold (Vm):**  
The point where Vin = Vout.  
This defines the inverter’s logic threshold and affects noise margins and delay.

---

## 4. Transient Behavior: Rise / Fall Delays

### Objective
To analyze the inverter’s transient response and extract propagation delays for rising and falling transitions.

### Description
A pulse input was applied to the inverter to measure output transitions.

### Results
**Rise delay:** 0.33 ps  
**Fall delay:** 0.28 ps  

![Transient_Plot_out_vs_time_in_with_Rise_Delay](/week_4/Deliverables/day_3/Labs_Sky130_SPICE_Simulation_for_CMOS/Transient_Plot_out_vs_time_in_with_Rise_Delay.png)  
![Transient_Plot_out_vs_time_in_with_Fall_Delay](/week_4/Deliverables/day_3/Labs_Sky130_SPICE_Simulation_for_CMOS/Transient_Plot_out_vs_time_in_with_Fall_Delay.png)

**Observation:**  
The PMOS, being weaker for the same W/L, results in longer rise time compared to fall time.  
These propagation delays are analogous to timing arcs analyzed in STA.

---

## 5. Noise Margin / Robustness Analysis

### Objective
To determine the noise margins from the VTC plot and evaluate the inverter’s robustness.

### Description
From the VTC curve, the following points were extracted:
- **VOH, VOL**: Output high/low levels  
- **VIH, VIL**: Input high/low thresholds

### Result
![Noise_Margin_Lab](/week_4/Deliverables/day_4/Sky130_Noise_Margin_Labs/Noise_Margin_Lab.png)

| Parameter | Value (V) |
|------------|------------|
| NMH = VOH - VIH | **0.75 V** |
| NML = VIL - VOL | **0.64 V** |

**Observation:**  
The inverter has sufficient noise margins for reliable logic levels.  
High NMH and NML ensure immunity to small voltage fluctuations.

---

## 6. Power-Supply and Device Variation Studies

### Objective
To analyze the effect of supply voltage and device sizing on inverter behavior.

### (a) Power Supply Variation)
Simulated VTC for multiple Vdd values (0.8V–1.8V).

![Plot_and_1o8V_Gain](/week_4/Deliverables/day_5/Sky130_Supply_Variation_Labs/Plot_and_1o8V_Gain.png)
![Plot_and_1o6V_Gain](/week_4/Deliverables/day_5/Sky130_Supply_Variation_Labs/Plot_and_1o6V_Gain.png)
![Plot_and_1o4V_Gain](/week_4/Deliverables/day_5/Sky130_Supply_Variation_Labs/Plot_and_1o4V_Gain.png)
![Plot_and_1o2V_Gain](/week_4/Deliverables/day_5/Sky130_Supply_Variation_Labs/Plot_and_1o2V_Gain.png)
![Plot_and_1V_Gain](/week_4/Deliverables/day_5/Sky130_Supply_Variation_Labs/Plot_and_1V_Gain.png)
![Plot_and_o8V_Gain](/week_4/Deliverables/day_5/Sky130_Supply_Variation_Labs/Plot_and_o8V_Gain.png)

| Vdd (V) | Gain |
|------------|------------|
| 1.8 | **7.4999** |
| 1.6 | **8.4430** |
| 1.4 | **9.8089** |
| 1.2 | **10.010** |
| 1.0 | **9.4985** |
| 0.8 | **8.9930** |


**Observation:**  
The gain increases up to 1.2 V but drops afterward.  
At lower Vdd, transistors do not fully switch ON, degrading noise margins and gain.

---

### (b) Device Sizing Variation
![Device_Variation_Lab_Plot](/week_4/Deliverables/day_5/Sky130_Device_Variation_Labs/Device_Variation_Lab_Plot.png)

**Observation:**  
With increased PMOS sizing, the high logic level holds longer than low logic.  
The switching threshold shifts to **~0.988 V**, demonstrating sensitivity to transistor ratio (β ratio).

---

## Summary of Extracted Parameters

| Parameter | Value |
|------------|--------|
| Threshold Voltage (Vt) | Extracted from Id–Vgs plot |
| Rise Delay | 0.33 ps |
| Fall Delay | 0.28 ps |
| NMH | 0.75 V |
| NML | 0.64 V |
| Switching Threshold (Vm) | ~0.988 V |

---

## Analysis & Discussion

- **Device Physics Insight:**  
  Channel-length modulation, velocity saturation, and W/L ratio directly affect Id–Vds and inverter delay.
- **STA Relevance:**  
  Propagation delays, threshold shifts, and voltage variations correspond to real STA timing variations.
- **Variation Impact:**  
  Changes in supply or device dimensions alter the inverter’s switching point and margins, affecting path delay and setup/hold constraints.

---

## Conclusion

This lab demonstrates how transistor-level characteristics translate to system-level timing behavior.  
By simulating MOSFET and CMOS circuits under varying conditions, we observe how:
- Physical effects dictate timing and noise robustness.
- Supply and sizing variations alter performance.
- These real effects underpin STA concepts like slack, delay, and margin.

Overall, this exercise bridges **device-level understanding** and **timing analysis**, reinforcing the importance of variation-aware design in CMOS technology.

---

**References:**
- [Sky130 Circuit Design Workshop](https://github.com/kunalg123/sky130CircuitDesignWorkshop/)
- VSD-IAT Platform

