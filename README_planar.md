# FPGA Camera Output HEX to Video Pipeline

## Overview
Converts raw FPGA HEX data into frames, images, and video for easy visualization and debugging.

---

## Objective
Convert raw FPGA data into usable visual formats:
HEX → Frames → Images → Video

---

## Processing Pipeline
HEX Input → Frame Extraction → Pixel Decode → Image Reconstruction → Outputs

---

## Frame Extraction
- Detects frame boundary using: F00F
- Splits continuous HEX stream into frames
- Each frame corresponds to one image (640×480)

---

## Project Structure
project/
├── input/
├── output/
│   ├── images/
│   ├── videos/
├── src/
└── README.md

---

## Outputs
- Normal Image (PNG)
- Normal Video (MP4)
- Inverted Image
- Inverted Video

---

## Tech Stack
- Python
- NumPy
- OpenCV
- PIL

---

## Performance
- Processing Time: 60 min → 10 min
- Improvement: ~83%

---

## Conclusion
Transforms raw FPGA HEX data into visual outputs for faster debugging and validation.
