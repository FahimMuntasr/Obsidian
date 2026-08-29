# EEE241L – Electrical Circuits II Laboratory

# Lab Report 3: Series RLC Circuits
---

# Objectives

The objectives of this experiment were:

- To investigate the characteristics of series RC, RL and RLC circuits.
- To study the relationship between voltage, current, impedance and phase angle in AC circuits.
- To verify the theoretical behavior of RC, RL and RLC circuits through practical measurements.
- To compare theoretical calculations with experimentally measured values.

---

# Equipment

| Sl. | Equipment |
|------|-----------|
| 1 | Breadboard |
| 2 | 100 Ω Resistor |
| 3 | 1 μF Capacitor |
| 4 | 330 μH Inductor |
| 5 | Function Generator |
| 6 | Digital Storage Oscilloscope (DSO) |
| 7 | Digital Multimeter (DMM) |
| 8 | LCR Meter |
| 9 | Connecting Wires |

---

# Theory

Alternating Current (AC) circuits differ from Direct Current (DC) circuits because they contain impedance rather than only resistance. Impedance represents the total opposition offered to alternating current and consists of both resistance and reactance.

The impedance of an AC circuit is given by
$$Z = R + jX$$
where

- \(R\) = Resistance (Ω)
- \(X\) = Reactance (Ω)

The magnitude of impedance is
$$|Z|=\sqrt{R^2+X^2}$$
The phase angle between the source voltage and current is
$$\theta=\tan^{-1}\left(\frac{X}{R}\right)$$
The capacitive reactance is
$$X_C=\frac{1}{2\pi fC}$$
where

- \(f\) = Frequency (Hz)
- \(C\) = Capacitance (F)

The inductive reactance is

$$X_L=2\pi fL$$
where

- \(L\) = Inductance (H)

According to AC Ohm's Law,

$$I=\frac{V}{Z}$$
### RC Circuit

In a series RC circuit,

- Current leads the capacitor voltage by 90°.
- The resistor voltage remains in phase with the current.
- The source voltage is the vector sum of \(V_R\) and \(V_C\).

### RL Circuit

In a series RL circuit,

- The inductor voltage leads the current by 90°.
- The resistor voltage remains in phase with the current.
- The source voltage is the vector sum of \(V_R\) and \(V_L\).

### RLC Circuit

For a series RLC circuit,
$$X=X_L-X_C$$
If
$$X_L>X_C$$
the circuit behaves inductively.
If
$$X_C>X_L$$
the circuit behaves capacitively.

When
$$X_L=X_C$$

the circuit reaches resonance, where the impedance becomes minimum and the current becomes maximum.

---

# Circuit Diagrams

Draw the following circuit diagrams neatly by hand.

1. Series RC Circuit
2. Series RL Circuit
3. Series RLC Circuit

(Use the diagrams provided in the laboratory manual.)

---

# Sample Calculations

## Given (Measured Values)

Resistance,
$$R=99.0\Omega$$
Capacitance,
$$C=0.971\mu F$$
Inductance,
$$L=342\mu H$$
Frequency,
$$f=10kHz$$
Source Voltage,
$$V_s=3V_{peak}$$
---

## Series RC Circuit

Capacitive Reactance,
$$X_C=\frac{1}{2\pi fC}$$
$$=\frac{1}{2\pi(10000)(0.971\times10^{-6})}$$
$$=16.40\Omega$$
Impedance,
$$|Z|=\sqrt{99^2+16.4^2}$$
$$=100.35\Omega$$
Phase Angle,
$$\theta
=
-\tan^{-1}
\left(
\frac{16.4}{99}
\right)$$
$$=-9.40^\circ$$
---

## Series RL Circuit

Inductive Reactance,
$$X_L
=
2\pi fL$$
$$=
2\pi(10000)(342\times10^{-6})$$
$$=
21.49\Omega$$
Impedance,
$$|Z|
=
\sqrt{99^2+21.49^2}$$
$$=
101.30\Omega$$
Phase Angle,
$$\theta
=
\tan^{-1}
\left(
\frac{21.49}{99}
\right)$$
$$=
12.24^\circ$$

---
## Series RLC Circuit

Net Reactance,

$$X=X_L-X_C$$
$$=20.70-16.00$$
$$=4.70\Omega$$


Impedance,
$$|Z|
=
\sqrt{99^2+4.70^2}$$
$$=
99.11\Omega$$

Phase Angle,
$$\theta
=
\tan^{-1}
\left(
\frac{4.70}{99}
\right)$$
$$=
2.72^\circ$$
# Data and Readings

## Table 1.1: Reactance and Impedance Values (Series RC Circuit)

| R (Measured) (Ω) | C (Measured) (F) | XC (Theory) (Ω) | \|Z\| (Ω) | ∠Z |
|-----------------:|-----------------:|----------------:|----------:|----:|
| 99.0 Ω | 0.971 μF | −16.40 Ω | 100.347 Ω | −9.40° |

---

## Table 1.2: Comparing Magnitudes and Phases of VC and VR

| Quantity | \|Vpeak\| (Theory) | θ (Theory) | \|Vpeak\| (Practical) | Delay ΔT | θ (Practical) | % Difference \|V\| | % Difference θ |
|----------|-------------------:|-----------:|----------------------:|----------:|--------------:|-------------------:|---------------:|
| VC | 500 mV | 80.60° | 504 mV | 22.4 μs | 80.64° | 0.80% | 0.05% |
| VR | 2.99 V | 9.40° | 2.84 V | 2 μs | 7.20° | 5.02% | 23.40% |

---

## Table 1.3: Reactance and Impedance Values (Series RL Circuit)

| R (Measured) (Ω) | L (Measured) (H) | XL (Theory) (Ω) | \|Z\| (Ω) | ∠Z |
|-----------------:|-----------------:|----------------:|----------:|----:|
| 99.0 Ω | 342 μH | 21.49 Ω | 101.30 Ω | 12.24° |

---

## Table 1.4: Comparing Magnitudes and Phases of VL and VR

| Quantity | \|Vpeak\| (Theory) | θ (Theory) | \|Vpeak\| (Practical) | Delay ΔT | θ (Practical) | % Difference \|V\| | % Difference θ |
|----------|-------------------:|-----------:|----------------------:|----------:|--------------:|-------------------:|---------------:|
| VL | 0.609 V | 77.76° | 574 mV | 19.2 μs | 69.12° | 5.75% | 11.11% |
| VR | 2.937 V | 12.24° | 2.76 V | 2 μs | 7.20° | 6.03% | 41.18% |

---

## Table 1.5: Reactance and Impedance Values (Series RLC Circuit)

| R (Measured) | C (Measured) | L (Measured) | XC (Theory) | XL (Theory) | \|Z\| | ∠Z |
|--------------:|-------------:|-------------:|------------:|------------:|------:|----:|
| 99.0 Ω | 0.971 μF | 342 μH | −16.00 Ω | 20.70 Ω | 99.113 Ω | 2.72° |

---

## Table 1.6: Comparing Magnitudes and Phases of VC, VL and VR


| Quantity | \|Vpeak\| (Theory) | θ (Theory) | \|Vpeak\| (Practical) | Delay ΔT | θ (Practical) | % Difference \|V\| | % Difference θ |
|----------|-------------------:|-----------:|----------------------:|----------:|--------------:|-------------------:|---------------:|
| VC | 0.484 V | 87.28° | 0.478 V | 24.1 μs | 86.76° | 1.24% | 0.60% |
| VR | 3.000 V | 2.72° | 2.95 V | 0.8 μs | 2.88° | 1.67% | 5.88% |
| VL | 0.627 V | 92.72° | 0.616 V | 25.7 μs | 92.52° | 1.75% | 0.22% |

---
# Questions and Answers

## Question 1

**In step 6, what would have happened if the required readings had been obtained by switching the positions of the resistor and the capacitor? Explain your answer.**

### Answer

Switching the positions of the resistor and capacitor in a series RC circuit would not change the circuit current because the components remain connected in series. Therefore, the theoretical voltage drops across the resistor and capacitor would remain unchanged.

However, the oscilloscope probes are connected with respect to specific circuit nodes. If the resistor and capacitor were interchanged without changing the probe connections, the measured voltage would correspond to a different component, leading to incorrect voltage and phase measurements. The oscilloscope setup would therefore need to be modified accordingly to obtain the correct readings.

---

## Question 2

**Draw the phasor diagrams for the circuits in Fig. B.1.1, Fig. B.1.2 and Fig. B.1.3.**

### Answer

The following phasor diagrams should be drawn neatly by hand.

### (a) Series RC Circuit

- Draw the current **I** as the reference along the positive x-axis.
- Draw the resistor voltage **VR** in phase with the current.
- Draw the capacitor voltage **VC** 90° below the current.
- The source voltage **VS** is the vector sum of **VR** and **VC**.

---

### (b) Series RL Circuit

- Draw the current **I** as the reference.
- Draw **VR** in phase with the current.
- Draw **VL** 90° above the current.
- Draw **VS** as the vector sum of **VR** and **VL**.

---

### (c) Series RLC Circuit

- Draw **VR** along the positive x-axis.
- Draw **VL** upward.
- Draw **VC** downward.
- The net reactive voltage is given by **VL − VC**.
- The source voltage **VS** is the vector sum of **VR** and the resultant reactive voltage.

---

## Question 3

**How would each of the phasor diagrams change if the source frequency was increased?**

### Answer

Increasing the source frequency affects the reactance of both inductors and capacitors.

For a capacitor,

$$X_C=\frac{1}{2\pi fC}$$

Therefore, increasing frequency decreases the capacitive reactance. As a result, the capacitor voltage becomes smaller and the phase angle decreases.

For an inductor,
$$X_L=2\pi fL$$

Increasing frequency increases the inductive reactance. Consequently, the voltage across the inductor increases and the circuit becomes more inductive.

In a series RLC circuit, the overall phase angle depends on the difference between inductive and capacitive reactance.

- If \(X_L>X_C\), the circuit becomes more inductive and the phase angle increases.
- If \(X_C>X_L\), the circuit behaves capacitively.
- At resonance, where \(X_L=X_C\), the reactive voltages cancel each other and the phase angle becomes approximately zero.

---

## Question 4

**In the case of the series RLC circuit, do the practical readings confirm the theoretical values? If any of the percentage differences are above 10%, suggest three possible reasons for the discrepancy.**

### Answer

Yes. The practical readings are generally in good agreement with the theoretical calculations. The measured voltages and phase angles closely follow the expected theoretical values, with only small deviations that fall within acceptable laboratory error.

Possible reasons for discrepancies greater than 10% include:

1. Manufacturing tolerances of the resistor, capacitor and inductor.
2. Internal resistance and non-ideal characteristics of the function generator, oscilloscope probes and measuring instruments.
3. Contact resistance of the breadboard and connecting wires, which may introduce additional voltage drops and phase shifts.

---

# Discussion

In this experiment, the behavior of series RC, RL and RLC circuits was investigated using a function generator and a digital storage oscilloscope. The practical values of the resistor, capacitor and inductor were first measured using the appropriate measuring instruments and were then used in all theoretical calculations.

For the series RC circuit, the measured resistor and capacitor values were found to be 99.0 Ω and 0.971 μF, respectively. The calculated impedance was approximately 100.35 Ω with a phase angle of −9.4°. The practical voltage measurements were found to be very close to the theoretical values, showing only a small percentage difference. The measured capacitor voltage lagged the source voltage as predicted by AC circuit theory.

In the series RL circuit, the measured inductance was 342 μH. The calculated inductive reactance and impedance closely matched the practical observations. The voltage across the inductor was observed to lead the current, while the resistor voltage remained in phase with the current. The measured values showed reasonable agreement with the theoretical calculations.

For the series RLC circuit, both inductive and capacitive reactances were present. Since the inductive reactance was slightly greater than the capacitive reactance, the circuit behaved as a slightly inductive circuit with a very small overall phase angle. The theoretical impedance was approximately 99.11 Ω, indicating that the circuit operated close to resonance.

Small differences between theoretical and practical values were observed throughout the experiment. These differences are expected because practical components are not ideal. Component tolerances, internal resistance of measuring instruments, parasitic capacitance and inductance of the breadboard, loose wire connections and slight errors while placing the oscilloscope cursors all contribute to measurement uncertainty.

Overall, the experimental results successfully verified the theoretical concepts of AC impedance, reactance and phase relationships in series RC, RL and RLC circuits.

---

# Conclusion

The objectives of this experiment were successfully achieved. The behavior of series RC, RL and RLC circuits was studied by comparing theoretical calculations with practical measurements obtained using a Digital Storage Oscilloscope.

The experimental results closely matched the theoretical predictions, confirming the relationships between resistance, reactance, impedance and phase angle in AC circuits. The series RC circuit exhibited capacitive behavior, while the series RL circuit exhibited inductive behavior. The series RLC circuit demonstrated the combined effect of inductive and capacitive reactance, producing a comparatively small phase angle because the inductive and capacitive reactances partially cancelled each other.

Although minor differences were observed between theoretical and practical values, these deviations were within acceptable limits and can be attributed to component tolerances, instrument limitations and unavoidable experimental errors.

Therefore, the experiment successfully verified the theoretical principles governing series RC, RL and RLC circuits.

---