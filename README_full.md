# 🚀 FPGA Camera Output HEX to Video Pipeline

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Domain](https://img.shields.io/badge/Domain-FPGA%20%7C%20Image%20Processing-green)
![Performance](https://img.shields.io/badge/Speed-83%25%20Faster-brightgreen)

---

## 📌 Overview
This project converts raw FPGA HEX data into images and video for debugging and validation.

---

## ❓ Problem
FPGA camera output is:
- Raw HEX stream  
- No visualization  
- Hard to debug  

---

## 🎯 Solution
HEX → Frames → Images → Video

---

## 🧠 Architecture

<div align="center">

<svg width="100%" height="300" viewBox="0 0 800 300" xmlns="http://www.w3.org/2000/svg">
<style>
.box { fill:#161b22; stroke:#58a6ff; stroke-width:1.5; rx:10; }
.text { fill:#c9d1d9; font-size:12px; text-anchor:middle; }
.arrow { stroke:#58a6ff; stroke-width:2; fill:none; }
</style>

<defs>
<marker id="arrow" markerWidth="10" markerHeight="10" refX="6" refY="3" orient="auto">
<polygon points="0 0, 6 3, 0 6" fill="#58a6ff"/>
</marker>
</defs>

<rect class="box" x="20" y="120" width="120" height="60"/>
<text x="80" y="150" class="text">HEX Input</text>

<rect class="box" x="180" y="120" width="140" height="60"/>
<text x="250" y="150" class="text">Frame Extract</text>

<rect class="box" x="360" y="120" width="140" height="60"/>
<text x="430" y="150" class="text">Decode</text>

<rect class="box" x="540" y="120" width="140" height="60"/>
<text x="610" y="150" class="text">Reconstruct</text>

<line class="arrow" x1="140" y1="150" x2="180" y2="150" marker-end="url(#arrow)"/>
<line class="arrow" x1="320" y1="150" x2="360" y2="150" marker-end="url(#arrow)"/>
<line class="arrow" x1="500" y1="150" x2="540" y2="150" marker-end="url(#arrow)"/>

</svg>

</div>

---

## ⚙️ Steps

1. HEX Input  
2. Frame Extraction (F00F marker)  
3. Pixel Decode  
4. Image Reconstruction  

---

## 📂 Output

- PNG Images  
- MP4 Video  
- Inverted versions  

---

## 📦 Tech Stack

- Python  
- NumPy  
- OpenCV  

---

## 🚀 Performance

- 60 min → 10 min  
- **83% faster**

---

## 🏁 Conclusion

Transforms raw FPGA data into usable visual output.
