<p align="center">
  <img src="https://github.com/syedfaqeeh/CNC-Laser-Machine/assets/your_image_here.png" alt="CNC Laser Machine Banner" width="600"/>
</p>

<h1 align="center">🛠️ DIY CNC Laser Machine</h1>

<p align="center">
  An open-source, low-cost CNC laser engraving machine for makers, students, and engineers. Fully documented with design files, electronics, and firmware setup.
</p>

<p align="center">
  <a href="LICENSE"><img alt="License" src="https://img.shields.io/badge/License-MIT-blue.svg" /></a>
  <img alt="Status" src="https://img.shields.io/badge/status-active-brightgreen.svg" />
  <a href="https://github.com/syedfaqeeh/CNC-Laser-Machine/issues"><img alt="Issues" src="https://img.shields.io/github/issues/syedfaqeeh/CNC-Laser-Machine" /></a>
  <a href="https://github.com/syedfaqeeh/CNC-Laser-Machine/stargazers"><img alt="Stars" src="https://img.shields.io/github/stars/syedfaqeeh/CNC-Laser-Machine" /></a>
</p>

---

## 📦 Bill of Materials (BoM)

<div align="center">

<table>
  <thead>
    <tr>
      <th align="left">Component</th>
      <th align="center">Quantity</th>
      <th align="left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Arduino UNO</td>
      <td align="center">1</td>
      <td>Main microcontroller</td>
    </tr>
    <tr>
      <td>CNC Shield v3</td>
      <td align="center">1</td>
      <td>Stepper interface board</td>
    </tr>
    <tr>
      <td>A4988 Drivers</td>
      <td align="center">2–3</td>
      <td>Motor drivers</td>
    </tr>
    <tr>
      <td>NEMA 17 Stepper Motors</td>
      <td align="center">2–3</td>
      <td>For X and Y axes</td>
    </tr>
    <tr>
      <td>Diode Laser Module</td>
      <td align="center">1</td>
      <td>500–700 mW laser</td>
    </tr>
    <tr>
      <td>12V Power Supply</td>
      <td align="center">1</td>
      <td>At least 3A output</td>
    </tr>
    <tr>
      <td>GT2 Timing Belts</td>
      <td align="center">As needed</td>
      <td>Motion control</td>
    </tr>
    <tr>
      <td>Linear Rails/Bearings</td>
      <td align="center">As needed</td>
      <td>For smooth movement</td>
    </tr>
    <tr>
      <td>MDF / Acrylic Base</td>
      <td align="center">1</td>
      <td>Frame and mount structure</td>
    </tr>
  </tbody>
</table>

</div>


---

## 🔍 Project Overview

This CNC laser machine is built with open-source hardware and software. It uses a diode laser for cutting or engraving, controlled via G-code from an Arduino-based controller.

<p align="center">
  <img src="https://github.com/syedfaqeeh/CNC-Laser-Machine/assets/your_build_image.png" alt="CNC Machine Closeup" width="500"/>
</p>

---

## 🧠 Features

- ✅ Budget-friendly and beginner-friendly
- ✅ Uses GRBL firmware and Arduino UNO
- ✅ Designed for wood, acrylic, and light materials
- ✅ Expandable and modifiable frame
- ✅ Compatible with LaserGRBL, UGS, etc.

---

## ⚙️ Wiring and Circuit Setup

<p align="center">
  <img src="https://github.com/syedfaqeeh/CNC-Laser-Machine/assets/your_circuit_diagram.png" alt="Wiring Diagram" width="600"/>
</p>

1. Connect Arduino UNO with CNC Shield.
2. Plug A4988 drivers with heat sinks.
3. Wire motors to the X and Y axis outputs.
4. Connect the diode laser to D11 (PWM spindle).
5. Connect external 12V power supply for motors and laser.

---

## 🖥️ Firmware & Software

- Flash **GRBL** to Arduino UNO.
- Use **LaserGRBL** or **Universal Gcode Sender** to send commands.
- Configure GRBL parameters for motion and laser PWM.

<details>
<summary>🔧 Sample GRBL Configuration</summary>

```bash
$32=1       ; Laser mode ON
$30=1000    ; Max spindle speed
$100=80     ; X steps/mm
$101=80     ; Y steps/mm
$110=2000   ; Max feedrate X
$111=2000   ; Max feedrate Y
