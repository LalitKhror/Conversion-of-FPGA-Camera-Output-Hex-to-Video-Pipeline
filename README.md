# 🚀 FPGA Camera Output HEX to Video Pipeline

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Domain](https://img.shields.io/badge/Domain-FPGA%20%7C%20Image%20Processing-green)
![Performance](https://img.shields.io/badge/Speed-83%25%20Faster-brightgreen)

⏱ **Processing Time Reduced:** 60 minutes → 10 minutes (≈83% faster)

---

## 📌 Overview

This project converts **raw FPGA camera HEX output** into structured frames, grayscale images, and MP4 video.

Developed during an internship, it helps in:
- Visual debugging of FPGA pipelines  
- Validating image data flow  
- Converting hardware data into human-readable format  

---

## ❓ Problem Statement

FPGA camera systems output:

- Raw HEX pixel streams  
- No direct visualization  
- No frame separation  
- Difficult debugging  

---

## 🎯 Objective

Convert raw FPGA HEX data into usable visual outputs:

HEX → Frames → Images → Video

---

## 🧠 System Architecture

👉 **Interactive View (Recommended):**  
[Open Architecture HTML]( https://lalitkhror.github.io/Conversion-of-FPGA-Camera-Output-Hex-to-Video-Pipeline/)

👉 **Static Diagram (PNG):**  

<img width="1482" height="586" alt="Architecture" src="https://github.com/user-attachments/assets/e7562892-c25f-4839-9d38-33df4b399c25" />


---

## 🔄 Processing Pipeline

HEX Input → Frame Extraction → Pixel Decode → Image Reconstruction → Outputs

### Explanation:
- **HEX Input** → Raw pixel stream from FPGA  
- **Frame Extraction** → Separates frames using markers  
- **Pixel Decode** → Converts HEX → intensity values  
- **Reconstruction** → Builds 2D image  
- **Outputs** → Images + Videos  

---

## 🧩 Frame Extraction

Frame boundaries are detected using a repeating marker:

FABC F123  

### How it works:
- Scan full HEX stream  
- Detect marker pattern  
- Split data into chunks  
- Each chunk = one frame (640 × 480)  

---

## 📂 Data Format

- Pixel Format: **16-bit HEX**  
- Resolution: **640 × 480**  
- Pixels per Frame: **307,200**  
- Frame Marker: **F00F**  

---

## ⚙️ Steps

1. Read HEX data  
2. Detect frame boundaries  
3. Decode pixel values  
4. Reconstruct image  
5. Generate outputs  

---

## 📁 Project Structure
```
project
│
├── input
│   └── Raw HEX input files
│
├── output
│   │
│   ├── images
│   │   ├── normal        (Normal grayscale images)
│   │   └── inverted      (Inverted grayscale images)
│   │
│   └── videos
│       ├── normal.mp4
│       └── inverted.mp4
│
├── src
│   └── pipeline.py       (Processing script)
│
├── docs
│   ├── index.html        (Interactive visualization)
│   └── Architecture.png  (Static diagram)
│
└── README.md
```

---

## 📦 Tech Stack

- Python  
- NumPy  
- OpenCV  
- Pillow (PIL)  

---

## 🚀 Performance

- Processing Time: **60 min → 10 min**  
- Improvement: **~83% faster**  

---

## 🔍 Use Cases

- FPGA image pipeline validation  
- Hardware debugging  
- Sensor data visualization  
- Pre-processing for computer vision  

---

## ⚠️ Limitations

- Fixed resolution (640×480)  
- Batch processing only  
- Grayscale only (no RGB yet)  

---

## 🔮 Future Work

- RGB (24-bit) support  
- Real-time pipeline  
- GPU acceleration  
- Binary input support  

---

## 🏁 Conclusion

This project bridges the gap between **raw FPGA output** and **visual understanding**, making debugging and validation significantly faster and easier.

---

## 👨‍💻 Author

Developed during Internship  
Focus: FPGA + Image Processing + System Design

