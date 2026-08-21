# RBMK-1000 Reactor Control Simulator

![Project Screenshot](raa.jpeg)

A browser-based simulation of an RBMK-1000 nuclear reactor core, developed using HTML, CSS, and JavaScript. This project provides an interactive control room interface featuring real-time telemetry, core channel management, and simplified reactor physics modeling, including the AZ-5 emergency shutdown protocol.

---

## Features

### Interactive Core Channel Map
*   **Circular Core Geometry:** The interface models the upper biological shield using a dynamic, mathematically bounded circular grid.
*   **Manual Control:** Click individual channels to insert or withdraw control rods and manage localized reactivity.
*   **Channel States:**
    *   **Dark Gray:** Withdrawn / Idle rods.
    *   **Amber:** Inserted / Active control rods (reduces reactivity).
    *   **Green:** Fixed graphite moderators (increases neutron flux).

### Real-Time Telemetry and Analytics
*   **Analog Gauges:** Visual indicators for Thermal Power, Reactivity Percentage, and Core Temperature.
*   **Live Data Charting:** Integrated Chart.js visualizations that monitor historical data continuously:
    *   Thermal Power (MW)
    *   Core Temperature (°C)
    *   Xenon-135 Concentration
*   **Control Room Log:** A real-time scrolling console that tracks operator actions, automated system responses, and system alerts.

### Reactor Controls
*   **Batch Operations:** Instantly insert or withdraw rods in increments of 10 to manage core output rapidly.
*   **AZ-5 (SCRAM):** Emergency defense protocol that simultaneously inserts all available control rods into the core.
*   **Autopilot:** An automated system toggle that manages rod positions to maintain safe thermal and power output parameters.
*   **System Reset:** Restores the reactor to its initial nominal standby state.

### Audio and Visual Alert System
*   **Status Monitoring:** The system dynamically transitions between NOMINAL, WARNING, DANGER, and FATAL states based on core temperature.
*   **Auditory Feedback:** Features authentic mechanical switches, alarm klaxons, and synthesized voice alerts for critical temperature thresholds.

### Simulated Reactor Physics
*   **Positive Void Coefficient:** Models the dangerous behavior where an increase in temperature creates steam voids, inadvertently increasing reactivity.
*   **Xenon Poisoning:** Simulates Xenon-135 buildup during operation, which acts as a neutron absorber and creates reactor stalling conditions.
*   **Graphite Tip Displacement:** accurately models the fatal design flaw of the RBMK reactor, where initiating an AZ-5 SCRAM causes a brief, massive spike in reactivity before the boron rods can engage.
*   **Thermal Thermodynamics:** Calculates heat generation versus passive cooling rates to determine core stability or catastrophic failure (meltdown).

---

## Usage

Simply open the `index.html` file in any modern web browser. No external dependencies or build steps are required, though an active internet connection is necessary to load the Chart.js library via CDN.