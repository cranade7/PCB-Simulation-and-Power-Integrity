# PCB Simulation and Power Integrity Enhancement Using Decoupling Capacitors

This project analyzes power and signal integrity in a multi-layer PCB using Cadence PowerSI. It simulates electromagnetic behavior before and after adding decoupling capacitors to improve voltage ripple and impedance characteristics.

## 📌 Objective

- Identify power/ground plane hot spots and unstable regions in a 5-layer PCB.
- Evaluate voltage ripple, Z-parameters, and 3D field simulations.
- Place decoupling capacitors in optimal locations to reduce ripple and improve power integrity.

## 🛠 Tools & Technologies

- **Simulation Software:** Cadence PowerSI
- **Core Principle:** Method of Moments (MoM) for solving Maxwell's equations
- **Design:** 5-layer PCB with 3 signal layers, 1 power plane, and 1 ground plane
- **Dielectric Constant (εr):** 6.5

## 🔧 Simulation Phases

### 🔹 Initial Setup
- Simulated a 100x100mm board layout without decoupling capacitors.
- Injected two AC excitation currents (100mA, 75mA).
- Added a 0.01 mΩ VRM short-circuit model for stress testing.

### 🔹 Results Without Capacitors
- Detected voltage ripple spikes at 150 MHz and 575 MHz.
- Voltage delta increased away from injection points, causing instability.
- Z-parameter plot showed significant peaks and dips, indicating poor power delivery.

### 🔹 Decoupling Capacitor Placement
- Hotspots identified using 3D spatial voltage plots.
- Capacitors placed strategically at high-voltage ripple regions.
- Resimulated board performance with capacitors added.

### 🔹 Results With Capacitors
- Voltage ripple at 150 MHz completely eliminated.
- Z-parameter peak dropped from ~15Ω to ~5Ω.
- Ripple reduced from 2.785V to 0.227V across the board.
- Spatial model max voltage dropped from 2.4V to 0.4V.

## 📈 Key Improvements

| Parameter                  | Without Caps | With Caps |
|---------------------------|--------------|-----------|
| Voltage Ripple (Max)      | 2.785 V      | 0.227 V   |
| Z-parameter (Peak)        | ~15 Ω        | ~5 Ω      |
| Voltage Max (Spatial Map) | 2.4 V        | 0.4 V     |

## ✅ Conclusion

By simulating and analyzing power integrity in a 5-layer PCB, this project demonstrates the critical role of decoupling capacitors. Strategic placement significantly improved system stability, making the board more reliable for high-speed communication and sensitive analog/digital operations.

