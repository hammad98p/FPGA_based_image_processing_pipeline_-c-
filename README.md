# Image Convolution Pipeline in C++ (FPGA-Oriented Design)

## Overview
This repository contains a C++ implementation of an image convolution pipeline built using object-oriented programming (OOP) principles.  
The design is inspired by FPGA-style architectures, focusing on modular pipeline stages, explicit memory handling, and dataflow-oriented processing.

The pipeline performs multiple image processing operations starting from color space conversion to edge detection and final image reconstruction.

NOTE: STD LIBRARY FILES ARE NOT INCLUDED IN THE REPO AND HENCE, REQUIRED TO BE DOWNLOADED FOR TESTING AND RUN. 

---

## Design Philosophy
- FPGA-inspired pipeline-based architecture
- Modular processing stages similar to hardware blocks
- Explicit buffer and memory management
- Clean OOP-based abstraction for extensibility

---

## Features
- Object-oriented C++ design using classes and structs
- Pixel-level and component-level data representation
- Dynamic memory allocation and deallocation to simulate register buffers
- Multi-stage image convolution pipeline
- Uses standard image loading and saving libraries

---

## Processing Pipeline
The image passes through the following stages:

1. **RGB to YCrCb Conversion**
   - Separates luminance and chrominance components

2. **Filtering Operations**
   - Gaussian filter for noise reduction  
   - Sharpening filter for detail enhancement  
   - Sobel filter for edge detection  

3. **Color Restoration**
   - YCrCb to RGB conversion after processing

4. **Output Generation**
   - Processed images are written to disk

---

## Implementation Details
- **Classes & Structs**
  - Used to define pixel values, image components, and processing methods
- **Register-like Buffers**
  - Dynamically allocated buffers simulate hardware registers
  - Explicit allocation and deletion of memory
- **Pipeline Stages**
  - Each stage is implemented as a modular processing unit

---

## Technologies Used
- **Language:** C++
- **Paradigm:** Object-Oriented Programming (OOP)
- **Libraries:** Standard image I/O libraries
- **Concepts:**  
  - Image convolution  
  - Color space transformation  
  - FPGA-oriented dataflow design  

---

## Future Improvements
- Porting the design to HLS (High-Level Synthesis)
- Introducing parallelism for hardware acceleration
- Using fixed-point arithmetic
- Mapping pipeline stages to real FPGA modules

---

## License
This project is intended for learning and experimentation.  
Feel free to use and extend it for educational or research purposes.
