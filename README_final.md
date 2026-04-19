# 🚀 FPGA Camera Output HEX to Video Pipeline

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Domain](https://img.shields.io/badge/Domain-FPGA%20%7C%20Image%20Processing-green)
![Performance](https://img.shields.io/badge/Speed-83%25%20Faster-brightgreen)

---

## 📌 Overview

This project converts **raw FPGA camera HEX output** into structured frames, grayscale images, and MP4 video.

Developed during an internship, it enables **visual debugging and validation** of FPGA-based image pipelines.

---

## ❓ Problem Statement

FPGA camera systems output:
- Raw HEX pixel streams  
- No visualization  
- No frame structure  
- Difficult debugging  

---

## 🎯 Objective

HEX Data → Frames → Images → Video

---

## 🧠 System Architecture

<div align="center">

<svg width="100%" height="560" viewBox="0 0 1200 560" xmlns="http://www.w3.org/2000/svg">
<style>
.box { fill:#161b22; stroke:#58a6ff; stroke-width:1.5; rx:12; }
.text { fill:#c9d1d9; font-size:12px; text-anchor:middle; }
.arrow { stroke:#58a6ff; stroke-width:2; fill:none; }
</style>

<defs>
<marker id="arrowhead" markerWidth="10" markerHeight="10" refX="6" refY="3" orient="auto">
<polygon points="0 0, 6 3, 0 6" fill="#58a6ff"/>
</marker>
</defs>

<rect width="1200" height="560" fill="#0d1117"/>

<rect class="box" x="50" y="250" width="150" height="70"/>
<text x="125" y="280" class="text">HEX Input</text>

<rect class="box" x="230" y="250" width="170" height="70"/>
<text x="315" y="280" class="text">Frame Extraction</text>

<rect class="box" x="430" y="250" width="160" height="70"/>
<text x="510" y="280" class="text">Decode</text>

<rect class="box" x="620" y="250" width="160" height="70"/>
<text x="700" y="280" class="text">Reconstruct</text>

<line class="arrow" x1="200" y1="285" x2="230" y2="285" marker-end="url(#arrowhead)"/>
<line class="arrow" x1="400" y1="285" x2="430" y2="285" marker-end="url(#arrowhead)"/>
<line class="arrow" x1="590" y1="285" x2="620" y2="285" marker-end="url(#arrowhead)"/>

</svg>

</div>

---

## 🔄 Pipeline

HEX → Frame Extraction → Decode → Reconstruction  
→ Images → Video  

---

## 📂 Data Format

- 16-bit HEX  
- 640 × 480  
- 307,200 pixels  
- Marker: F00F  

---

## ⚙️ Steps

1. HEX Input  
2. Frame Detection  
3. Decode  
4. Reconstruction  
5. Output  

---

## 📁 Structure

project/
├── input/
├── output/
├── src/
└── README.md

---

## 📦 Tech Stack

Python, NumPy, OpenCV, PIL  

---

## 🚀 Performance

60 min → 10 min (**83% faster**)  

---

## 🏁 Conclusion

Converts raw FPGA data into visual output for debugging.
