---
layout: default
title: Collaborations
---

# Collaborations

At Lippe Optics, we believe that innovation benefits from collaboration. Alongside developing our own technologies, our team also supports selected projects and initiatives by providing engineering knowledge, design assistance, and technical expertise.

## Partnering Projects

### Project 1 – Patient Monitoring System – Pager

**Area:** Engineering & Development  
**Collaboration:** Technical assistance and design support

Our team supported a local medical facility in developing a pager unit designed to be operated by nurses. The pager helps nurses monitor the status of patients by displaying relevant data such as heart rate and temperature.

Using data shared from other units through MQTT messages, the nurses can be alerted in real time in case of emergencies. By applying the MQTT knowledge gained during the development of the Mosquito Laser Targeting System, our team was able to further enhance the capabilities of the existing pager system at the medical facility.

<br>

<img src="{{ '/imgs/pager_unit.jpeg' | relative_url }}"
     alt="Patient monitoring pager unit"
     class="collaboration-image"
     onclick="openLightbox(this)">
</a>

### Project 2 – Custom 8-bit CPU

**Area:** VHDL & PCB Design  
**Collaboration:** Assistance with VHDL coding and PCB design

In collaboration with another company, an 8-bit CPU was developed for a specific application. Due to confidentiality requirements, further details about the product cannot be disclosed. Our team contributed to the development of the CPU, primarily supporting areas such as the **ALU, ROM, and RAM**.

Testing was performed on an FPGA to verify the functionality of the design, using tools including **Intel Questa** and **AMD Vivado**.

Furthermore, a custom PCB was developed for the project, incorporating all required components and features. This collaboration provided valuable experience for both teams and offered further insight into FPGA development, VHDL, and custom hardware design.

<br>

<img src="{{ '/imgs/vhdl.jpeg' | relative_url }}"
     alt="Custom 8-bit CPU development"
     class="collaboration-image"
     onclick="openLightbox(this)">


## Our Contribution

Our team can provide support in areas including:

<br>

- PCB and electronic design
- Embedded systems
- Mechanical and product design
- Software development
- Prototyping and testing
- Technical documentation
- Engineering consultation

## Interested in Collaborating?

We are open to working with students, engineers, designers, researchers, and other project teams who are interested in developing innovative technical solutions.

If you have a project that could benefit from our expertise, feel free to **get in touch with us**.

<div id="image-lightbox" class="image-lightbox" onclick="closeLightbox()">
  <span class="lightbox-close">&times;</span>
  <img id="lightbox-image" src="" alt="">
</div>

<script>
function openLightbox(image) {
  document.getElementById("lightbox-image").src = image.src;
  document.getElementById("image-lightbox").classList.add("active");
}

function closeLightbox() {
  document.getElementById("image-lightbox").classList.remove("active");
}
</script>