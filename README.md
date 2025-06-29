<h1 align="center">🛠️ DIY CNC Laser Machine</h1>

<p align="center">
  <img src="https://github.com/syedfaqeeh/CNC-Laser-Machine/blob/main/images/cnc%20pic1.jpg" alt="CNC Laser Machine Banner" width="600"/>
</p>

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
      <td>MKS-DLC32 Controler Board</td>
      <td align="center">1</td>
      <td>Main microcontroller</td>
    </tr>
    <tr>
      <td>MKS-TS35 Display</td>
      <td align="center">1</td>
      <td>Stepper interface board</td>
    </tr>
    <tr>
      <td>MKS TMC2209 V2.0 Drivers</td>
      <td align="center">3</td>
      <td>Motor drivers</td>
    </tr>
    <tr>
      <td>NEMA 17 Stepper Motors</td>
      <td align="center">4</td>
      <td>For X and Y axes</td>
    </tr>
    <tr>
      <td>80W Laser Module</td>
      <td align="center">1</td>
      <td>450 nm Wavelentth, 10W Laser</td>
    </tr>
    <tr>
      <td>12V Power Supply</td>
      <td align="center">1</td>
      <td>At least 10A output</td>
    </tr>
    <tr>
      <td>GT2 Timing Belts</td>
      <td align="center">7ft</td>
      <td>Motion control</td>
    </tr>
    <tr>
      <td>Linear Rails/Bearings</td>
      <td align="center">2</td>
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

This CNC laser machine is built with open-source hardware and software. It uses a diode laser for cutting or engraving, controlled via G-code from an ESP32-based controller.

<p align="center">
  <img src="https://github.com/syedfaqeeh/CNC-Laser-Machine/blob/main/videos/gifs/Laser1-ezgif.com-video-to-gif-converter.gif" alt="CNC Machine Closeup" width="500"/>
</p>

<p align="center">
Laser Cutting Operation
</p>
  
<p align="center">
  <img src="https://github.com/syedfaqeeh/CNC-Laser-Machine/blob/main/videos/gifs/Up2-ezgif.com-video-to-gif-converter.gif" alt="CNC Machine Closeup" width="500"/>
</p>



---

## 🧠 Features

- ✅ Budget-friendly and beginner-friendly
- ✅ Uses GRBL firmware and ESP32 controller board
- ✅ Designed for wood, acrylic, and light materials
- ✅ Expandable and modifiable frame
- ✅ Compatible with LaserGRBL, UGS, etc.

---

## ⚙️ Wiring and Circuit Setup

<p align="center">
  <img src="https://github.com/makerbase-mks/MKS-DLC32/blob/main/MKS-DLC32-main/images/interface.png" alt="Wiring Diagram" width="600"/>
</p>

1. Connect MKS-DLC32 with MKS-TS35.
2. Plug MKS TMC2209 drivers with heat sinks.
3. Wire motors to the X, Y and Z axis outputs.
4. Connect the diode laser (PWM spindle).
5. Connect external 12V power supply for motors and laser.

---

## 🖥️ Firmware & Software

- Flash **GRBL** to ESP32.
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
