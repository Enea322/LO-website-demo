---
layout: default
title: Patient Monitoring System – Pager
---

<article>

<p style="margin-bottom: 25px;">
  <a href="{{ '/blog.html' | relative_url }}"
     style="
       color:#1a3a52;
       text-decoration:none;
       font-weight:600;
     ">
    ← Back to Engineering Blog
  </a>
</p>

<h1 style="color:#1a3a52;">Patient Monitoring System - Pager</h1>

<p style="color:#777; font-size:0.95em;">
August 2026 · Embedded Systems · MQTT · Engineering
</p>

<hr>

<h2>Overview</h2>

<p>
The Patient Monitoring System is an engineering project focused on developing
a reliable communication system for transmitting notifications between a
monitoring system and a dedicated pager device.
</p>

<p>
The project combines embedded electronics, wireless communication, software
development, and user notification systems into a compact and practical
solution. The objective was to provide personnel with important status or
alert information without requiring them to remain directly next to the
monitoring equipment.
</p>

<h2>Motivation</h2>

<p>
In environments where continuous monitoring is required, important
notifications need to reach personnel quickly and reliably. A dedicated
notification device can provide a simple interface for receiving alerts while
allowing the user to remain mobile.
</p>

<p>
The project therefore explored how modern communication protocols and
embedded hardware could be combined to create a lightweight notification
system.
</p>

<h2>System Architecture</h2>

<p>
The system was designed around a monitoring device, a central MQTT broker,
and a dedicated pager unit. When a relevant event was detected, the
monitoring system transmitted the corresponding information through the
communication network.
</p>

<p>
A <strong>Raspberry Pi 4</strong> was used as the MQTT broker and served as
the central communication point between the monitoring system and the pager.
The pager itself was built around an <strong>ESP32</strong>, which acted as
the main processing and communication unit.
</p>

<div style="
background:#f5f5f5;
border:2px solid #1a3a52;
border-radius:10px;
padding:20px;
margin:25px 0;
text-align:center;
">
<strong>
Monitoring System → Raspberry Pi 4 (MQTT Broker) → ESP32 Pager
</strong>
<br><br>
LCD Display · LED · Buzzer
</div>

<p>
The modular architecture allowed the communication infrastructure and pager
hardware to be developed and tested independently before being integrated
into the complete system.
</p>

<h2>Pager Hardware</h2>

<p>
The pager prototype was built around an <strong>ESP32</strong>, which handled
the communication and processing required to receive and interpret incoming
notifications.
</p>

<p>
The pager consisted of several components designed to provide the user with
different forms of feedback:
</p>

<ul>
<li><strong>ESP32</strong> – processing and wireless communication</li>
<li><strong>16×2 LCD display</strong> – displaying received notifications</li>
<li><strong>LED</strong> – visual notification</li>
<li><strong>Buzzer</strong> – audible notification</li>
<li><strong>Small battery</strong> – portable power supply</li>
<li><strong>Breadboard</strong> – prototyping and component interconnection</li>
</ul>

<p>
The initial prototype was assembled on a breadboard. This made it possible to
quickly modify the circuit, test individual components, and troubleshoot
hardware connections during development.
</p>

<h2>MQTT Communication</h2>

<p>
MQTT was used as the communication protocol between the system components.
Its lightweight publish-subscribe architecture makes it well suited for
embedded applications where devices need to exchange relatively small
amounts of information.
</p>

<p>
The Raspberry Pi 4 operated as the MQTT broker. The monitoring system could
publish an event to a designated MQTT topic, while the ESP32 pager subscribed
to the relevant topic.
</p>

<p>
When a new notification was received, the ESP32 processed the message and
activated the appropriate pager components. The notification could therefore
be presented through the LCD display, LED, and buzzer.
</p>

<h2>Development Process</h2>

<p>
Development was approached incrementally. Individual hardware components
were first connected and tested before implementing the complete notification
logic.
</p>

<p>
The ESP32 communication functionality was then integrated with the MQTT
broker running on the Raspberry Pi 4. Once communication between the devices
was established, the LCD, LED, and buzzer were incorporated into the pager
logic.
</p>

<p>
Using a breadboard during this stage allowed the hardware configuration to
be changed easily as the system evolved.
</p>

<h2>Challenges</h2>

<p>
One of the main challenges was achieving reliable communication between the
monitoring system, MQTT broker, and pager. The system needed to correctly
handle incoming messages and translate them into appropriate user
notifications.
</p>

<p>
Hardware integration also required careful consideration of the connections
between the ESP32 and the different notification components.
</p>

<p>
Another consideration was the portable nature of the pager. The use of a
small battery introduced additional requirements regarding power consumption
and the practical operation of the device.
</p>

<h2>Testing and Evaluation</h2>

<p>
Testing focused on verifying communication between the system components and
ensuring that received MQTT messages resulted in the expected pager
behaviour.
</p>

<p>
The LCD display, LED, and buzzer were tested individually before being
combined into the complete notification system. The breadboard prototype
made it possible to identify and correct hardware and wiring issues during
this process.
</p>

<p>
As a prototype engineering project, the system was intended primarily for
development and demonstration rather than deployment as a certified medical
device.
</p>

<h2>Future Development</h2>

<p>
Future development could include a more compact custom PCB, improved power
management, a dedicated enclosure, additional notification functions, and
further improvements to the communication architecture.
</p>

<p>
The breadboard prototype could also be replaced with a more robust hardware
implementation suitable for long-term testing and practical deployment.
</p>

<h2>Conclusion</h2>

<p>
The Patient Monitoring System demonstrates how embedded electronics and
lightweight communication protocols can be combined to create a practical
notification platform.
</p>

<p>
By combining an ESP32-based pager with a Raspberry Pi 4 MQTT broker and
multiple notification interfaces, the project provided practical experience
in embedded programming, wireless communication, hardware integration, and
system-level engineering.
</p>

<p style="margin-top: 35px;">
  <a href="{{ '/blog.html' | relative_url }}"
     style="
       color:#1a3a52;
       text-decoration:none;
       font-weight:600;
     ">
    ← Back to Engineering Blog
  </a>
</p>

</article>