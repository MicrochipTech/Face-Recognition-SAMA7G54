

# Face Recognition with SAMA7G54

Real-time face detection demo running on a Microchip SAMA7G54 evaluation kit. The system captures live video input, identifies human faces, and reports their locations within each video frame.

---

## Table of Contents

- [Features](#features)  
- [Hardware Requirements](#hardware-requirements)  
- [Software Requirements](#software-requirements)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Troubleshooting](#troubleshooting)  
- [Version History](#version-history)  
- [Authors](#authors)  
- [License](#license)  

---

## Features

- Captures video input from a USB camera.  
- Performs real-time face detection on the SAMA7G54 MPU.  
- Outputs face bounding boxes or similar metadata.  
- Optimized for embedded performance.

---

## Hardware Requirements

- **Microchip SAMA7G54 Evaluation Kit** :contentReference[oaicite:0]{index=0}  
- USB camera compatible with the board :contentReference[oaicite:1]{index=1}  
- Host PC or terminal emulator to view debugging/log output via serial or USB connection :contentReference[oaicite:2]{index=2}  

---

## Software Requirements

- Boot firmware / image built for SAMA7G54 that includes support for USB camera input and face detection inference (e.g. Edge Impulse image / model) :contentReference[oaicite:3]{index=3}  
- Terminal emulator (e.g. TeraTerm) for console access :contentReference[oaicite:4]{index=4}  
- Appropriate drivers / power supply for the board as per Microchip’s user guide :contentReference[oaicite:5]{index=5}  

---

## Installation

* Follow [this guide](https://docs.edgeimpulse.com/docs/edge-ai-hardware/cpu/microchip-sama7) provided by Edge Impulse to flash the image on your Microprocessor.

1. Unpack the SAMA7G54 evaluation board, ensuring you observe ESD precautions.  
2. Check and set default jumper settings.  
3. Connect USB-micro-AB cable to the J24 (J-Link-OB USB) port.  
4. Connect the other end of that USB cable to your PC.  
5. Open a terminal emulator with settings `115200, N, 8, 1`.  
6. Power the board either by:  
   a. USB-micro-AB cable into J7 (USB-A port), or  
   b. AC/DC wall adapter into the DC jack connector.  
7. Reset the board. You should see a startup log on the console.  
8. Flash the face detection demo image (e.g. using Edge Impulse provided image) onto the SAMA7G54 according to the “Primary User Guide” (see page 66). :contentReference[oaicite:6]{index=6}  

---

## Usage

- After flashing and booting, ensure the USB camera is connected and recognized.  
- The demo will start running automatically (or via a command) and begin processing frames.  
- Monitor the console output (serial) to see detection results (e.g. coordinates of bounding boxes or number of faces).  
- Use any additional provided UI or indicators (if applicable) to view the face detection overlay.

---

## Troubleshooting

| Problem | Possible Cause | Solution |
|---|---|---|
| No console output | Board not powered / wrong serial settings / wrong port | Check connections, serial settings, and power source |
| USB camera not detected | Incompatible camera / insufficient power / driver support missing | Try a different camera, ensure USB power is adequate, verify driver support |
| Faces not detected or inaccurate | Model not well trained / lighting / camera angle | Improve lighting, adjust camera angle, retrain or fine-tune model |

---

## Version History

- **v0.1** – Initial release. Basic face detection working.  
- **v0.2** – Bug fixes and performance optimizations.  

---

## Authors

- Microchip Technology, Inc.  
- (Add any individual contributors here, if applicable.)

---

## License

Specify license here (e.g. MIT, Apache-2.0, etc.).  
(If you haven’t chosen one yet, pick a license and insert the text or link.)

---

## Acknowledgments

- Edge Impulse for image/model generation tools  
- Microchip SAMA7G54 documentation for hardware setup  
- Open source face detection libraries / prior art

---


