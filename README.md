
<div align="center">

<h1>🔋 ESP32 Based Lithium-Ion Battery Analyzer</h1>

<p>
An intelligent battery analyzer designed to evaluate Lithium-Ion battery health by
measuring voltage, capacity, internal resistance, and performing controlled constant-current discharge.
</p>

<img src="images/prototype.jpg" width="700" alt="Project Image">

<p>
<img src="https://img.shields.io/badge/ESP32-Microcontroller-red">
<img src="https://img.shields.io/badge/Language-C++-blue">
<img src="https://img.shields.io/badge/Platform-Arduino-green">
<img src="https://img.shields.io/badge/Status-Completed-success">
</p>

</div>

---

<h2>📖 About the Project</h2>

<p>
This project is an ESP32-based Battery Analyzer capable of automatically evaluating
Lithium-Ion batteries. The system performs voltage monitoring, constant current
discharge, battery capacity estimation, and internal resistance measurement while
displaying real-time information on an OLED display.
</p>

---

<h2>✨ Features</h2>

<ul>
<li>🔋 Automatic Battery Detection</li>
<li>📊 Real-Time Voltage Monitoring</li>
<li>⚡ Constant Current Discharge</li>
<li>📈 Capacity Measurement (mAh)</li>
<li>📉 Internal Resistance Measurement (mΩ)</li>
<li>🌡️ Temperature Controlled Cooling Fan</li>
<li>📟 OLED Live Display</li>
<li>🌐 ESP32 Wi-Fi Ready</li>
</ul>

---

<h2>🛠 Hardware Components</h2>

<table>
<tr>
<th>Component</th>
<th>Purpose</th>
</tr>

<tr>
<td>ESP32</td>
<td>Main Controller</td>
</tr>

<tr>
<td>ADS1115</td>
<td>16-bit ADC Voltage Measurement</td>
</tr>

<tr>
<td>LM358</td>
<td>Constant Current Controller</td>
</tr>

<tr>
<td>IRFZ44N</td>
<td>Electronic Load MOSFET</td>
</tr>

<tr>
<td>1Ω 10W Resistor</td>
<td>Current Sensing</td>
</tr>

<tr>
<td>OLED Display</td>
<td>User Interface</td>
</tr>

<tr>
<td>Mini360 Buck Converter</td>
<td>Voltage Regulation</td>
</tr>

<tr>
<td>Cooling Fan</td>
<td>Thermal Management</td>
</tr>

</table>

---

<h2>⚙️ Working Principle</h2>

<ol>

<li>
Battery voltage is measured using the ADS1115 ADC.
</li>

<li>
ESP32 generates a PWM signal which is converted into a reference voltage through a low-pass filter.
</li>

<li>
LM358 compares the reference voltage with the sensing resistor voltage and adjusts the MOSFET gate to maintain a constant discharge current.
</li>

<li>
Battery capacity is calculated from discharge current and elapsed time.
</li>

<li>
Internal resistance is calculated by comparing open-circuit voltage and loaded voltage.
</li>

<li>
Cooling fan automatically turns on when required.
</li>

</ol>

---

<h2>📂 Project Structure</h2>

<pre>
Battery-Analyzer/
│
├── firmware/
├── hardware/
├── circuit/
├── images/
├── docs/
└── README.md
</pre>

---

<h2>📸 Project Images</h2>

<p align="center">

<img src="images/prototype.jpg" width="45%">

<img src="images/circuit.jpg" width="45%">

</p>

---

<h2>🚀 Future Improvements</h2>

<ul>

<li>Battery Charging Module</li>

<li>Web Dashboard</li>

<li>Cloud Data Logging</li>

<li>CSV Export</li>

<li>Machine Learning Based Battery Health Prediction</li>

<li>Support for Multiple Battery Types</li>

</ul>

---

<h2>📚 Applications</h2>

<ul>

<li>Battery Repair Shops</li>

<li>Research Laboratories</li>

<li>Educational Projects</li>

<li>Quality Control</li>

<li>DIY Electronics</li>

</ul>

---

<h2>👨‍💻 Author</h2>

<b>Shahriar Kabir Saikat</b>

<br>

B.Sc. in Computer Science & Engineering

<br>

United International University (UIU)

<br><br>

⭐ If you like this project, consider giving it a Star.


