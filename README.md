<img width="1113" height="659" alt="image" src="https://github.com/user-attachments/assets/a06407dc-1b46-4984-9199-71a16e8dc074" />
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
<h2>🚨 Problem Statement</h2>

<p align="justify">

Lithium-Ion batteries are widely used in smartphones, laptops, electric vehicles,
power banks, drones, and IoT devices. Despite their widespread use, determining
the actual health of a battery remains a significant challenge.

Most affordable battery testers available in the market only display the battery
voltage. However, battery voltage alone cannot accurately determine the remaining
capacity or overall health of a battery. A battery may still show a normal voltage
while suffering from reduced capacity, increased internal resistance, and poor
performance under load.

Professional battery analyzers provide accurate measurements but are often
expensive, bulky, and inaccessible for students, hobbyists, repair technicians,
and educational laboratories.

</p>

<img src="images/mp_illusion.png" width="700" alt="illusion Image">
<p> trapped as a customer </p>
<img src="images/trap.png" width="700" alt="Project Image">
---

<h2>💡 Proposed Solution</h2>

<p align="justify">

This project presents a low-cost, portable, and open-source Battery Analyzer
powered by the ESP32 microcontroller.

The analyzer performs automated battery diagnostics by measuring multiple battery
health parameters instead of relying only on voltage. It combines precision
voltage sensing, constant-current discharge control, capacity estimation,
internal resistance calculation, and real-time monitoring into a single compact
device.

The system provides an affordable alternative to expensive commercial battery
analyzers while maintaining reliable measurement accuracy for educational,
research, and repair applications.

</p>

---

<h2>⭐ Why is this Different?</h2>

<p align="justify">

Unlike conventional low-cost battery testers, this project performs a complete
battery health analysis instead of displaying only battery voltage.

By integrating an ESP32, ADS1115 ADC, LM358 operational amplifier, and MOSFET-
based electronic load, the analyzer is capable of maintaining a stable constant
discharge current while calculating battery capacity and internal resistance in
real time and it can discharge or charge in the middle of the test and real time dashboard.

Its open-source architecture also allows developers and researchers to customize,
extend, and integrate additional features such as cloud monitoring, data logging,
and machine learning-based battery health prediction.

</p>

<img src="images/unique1.png" width="700" alt="Project Image">


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
<td>ESP32 DevKit</td>
<td>Main Controller & Data Processing</td>
</tr>

<tr>
<td>Perfboard</td>
<td>Circuit Assembly</td>
</tr>

<tr>
<td>18650 Battery Holder</td>
<td>Battery Connection</td>
</tr>

<tr>
<td>OLED SSD1306 Display</td>
<td>User Interface & Measurement Display</td>
</tr>

<tr>
<td>ADS1115 ADC Module</td>
<td>High-Precision Voltage Measurement</td>
</tr>

<tr>
<td>LM358 IC</td>
<td>Constant Current Control Circuit</td>
</tr>

<tr>
<td>8-Pin IC Socket</td>
<td>LM358 Mounting</td>
</tr>

<tr>
<td>IRLZ44N MOSFET</td>
<td>Electronic Load</td>
</tr>

<tr>
<td>1Ω 10W Power Resistor</td>
<td>Current Sensing</td>
</tr>

<tr>
<td>Heatsink</td>
<td>MOSFET Cooling</td>
</tr>

<tr>
<td>Thermal Paste</td>
<td>Improves Heat Transfer</td>
</tr>

<tr>
<td>Push Button</td>
<td>User Input / Menu Control</td>
</tr>

<tr>
<td>Buzzer</td>
<td>Audio Notifications</td>
</tr>

<tr>
<td>Green LED</td>
<td>Status Indicator</td>
</tr>

<tr>
<td>Red LED</td>
<td>Error / Warning Indicator</td>
</tr>

<tr>
<td>Blue/Yellow LED</td>
<td>Operation Status Indicator</td>
</tr>

<tr>
<td>220Ω, 470Ω, 4.7kΩ, 10kΩ, 33kΩ, 1MΩ Resistors</td>
<td>Voltage Divider & Signal Conditioning</td>
</tr>

<tr>
<td>104 Ceramic Capacitor</td>
<td>Noise Filtering</td>
</tr>

<tr>
<td>220µF Capacitor</td>
<td>Power Supply Stabilization</td>
</tr>

<tr>
<td>Male/Female Header Pins</td>
<td>Module Connections</td>
</tr>

<tr>
<td>4-Pin OLED Header</td>
<td>OLED Display Connection</td>
</tr>

<tr>
<td>2-Pin Screw Terminal</td>
<td>Battery Terminal Connection</td>
</tr>

<tr>
<td>Hook-up Wire</td>
<td>Electrical Wiring</td>
</tr>

<tr>
<td>Solder Wire</td>
<td>Circuit Assembly</td>
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

<p> charging system </p>
<img src="images/charge.png" width="700" alt="Charge Image">

<p> discharging system </p>
<img src="images/discharge.png" width="700" alt="Discharge Image">

<p> flow state </p>
<img src="images/flow.png" width="700" alt="flow Image">

---

<h2>📊 Comparison with Existing Battery Testers</h2>

<table>

<tr>
<th>Feature</th>
<th>Low-Cost Tester</th>
<th>Professional Analyzer</th>
<th>This Project</th>
</tr>

<tr>
<td>Voltage Measurement</td>
<td>✅</td>
<td>✅</td>
<td>✅</td>
</tr>

<tr>
<td>Capacity Estimation</td>
<td>❌</td>
<td>✅</td>
<td>✅</td>
</tr>

<tr>
<td>Internal Resistance Measurement</td>
<td>❌</td>
<td>✅</td>
<td>✅</td>
</tr>

<tr>
<td>Constant Current Discharge</td>
<td>❌</td>
<td>✅</td>
<td>✅</td>
</tr>

<tr>
<td>OLED Display</td>
<td>❌</td>
<td>✅</td>
<td>✅</td>
</tr>

<tr>
<td>ESP32 Wi-Fi Support</td>
<td>❌</td>
<td>Limited</td>
<td>✅</td>
</tr>

<tr>
<td>Open Source</td>
<td>❌</td>
<td>❌</td>
<td>✅</td>
</tr>

<tr>
<td>Affordable</td>
<td>✅</td>
<td>❌</td>
<td>✅</td>
</tr>

</table>

<img src="images/mid.png" width="700" alt="mid Image">

---

<h2>🎯 Project Objectives</h2>

<ul>

<li>Develop a low-cost Lithium-Ion Battery Analyzer.</li>

<li>Measure battery voltage with high precision.</li>

<li>Estimate actual battery capacity (mAh).</li>

<li>Measure internal resistance (mΩ).</li>

<li>Maintain constant current using an LM358 and MOSFET.</li>

<li>Display live battery information on an OLED display.</li>

<li>Provide an open-source platform for battery research and education.</li>

</ul>

---

<h2>🌍 Real-World Applications</h2>

<ul>

<li>🔋 Battery Repair & Refurbishment</li>

<li>📱 Smartphone & Laptop Battery Diagnostics</li>

<li>🚗 Electric Vehicle Battery Maintenance</li>

<li>🧪 Engineering Research Laboratories</li>

<li>🎓 University Projects & Education</li>

<li>⚡ DIY Electronics and Maker Communities</li>

<li>🏭 Battery Quality Inspection</li>

</ul>
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
<p> schematic circuit </p>

<p align="center">
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
<h2>📽️ Project Presentation</h2>

<p>
This repository includes the complete project presentation describing the problem,
system architecture, hardware design, working principle, implementation, and future improvements.
</p>

<a href="Slide/Battery_Analyzer_Presentation.pptx">
  📊 Battery Analyzer Presentation (PPTX)
</a>
---
<h2>📚 Applications</h2>

<ul>

<li>Battery Repair Shops</li>

<li>Research Laboratories</li>

<li>Educational Projects</li>

<li>Quality Control</li>

<li>DIY Electronics</li>

</ul>

<img src="images/beware.png" width="700" alt="mid Image">

Codes are available in the repo

---

<h2>👨‍💻 Author</h2>

<b>Shahriar Kabir Saikat</b>

<b>Sabiha Akter</b>

<b>Sayeda Sanjida Karim Sanjida</b>

<br>

B.Sc. in Computer Science & Engineering

<br>

United International University (UIU)

<br><br>

⭐ If you like this project, consider giving it a Star.


