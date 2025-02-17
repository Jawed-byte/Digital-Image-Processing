# 1. Fundamentals of Image and Video Processing from Scratch

## Overview
This project implements fundamental image and video processing techniques **without relying on high-level image processing libraries** (except for basic file I/O). The goal is to build an understanding of how images and videos are represented and manipulated at a low level.

## Features
- **Image Reading & Writing**: Implemented functions to read an image file into an array and write an array back to an image file.
- **Brightness & Contrast Adjustment**: Manipulated pixel values to adjust brightness and contrast dynamically.

- **Grayscale Conversion**: Developed multiple methods for converting a color image to grayscale and analyzed their visual effects.

- **Pseudo-Color Mapping**: Applied pseudo-coloring techniques to enhance grayscale images.
- **Green-Screen Background Replacement**: Extracted and replaced green backgrounds in an image with a different background image.

- **Video Processing Pipeline**:
  - Read a video file and convert it into a sequence of images.
  - Reconstruct the video from the sequence of images.
- **Transition Effects**: Created a 1-second transition effect (fade, slide, etc.) between two images.
- **Optimized Memory Usage**: Used efficient data structures and optimized processing techniques for handling large image and video files.

# 2. Fundamental Image Processing: Quantization, Histogram Equalization, Cryptography, and Transformations

## Overview
This project implements essential image processing techniques **without relying on high-level image processing libraries** (except for basic file I/O). The goal is to develop a deeper understanding of image representation and manipulation by implementing core techniques from scratch.

## Features
- **Image Quantization**: Reduced image size by quantizing it into 1-8 bit representations and analyzed the visual effects.


- **Histogram Equalization**:
  - Implemented a custom `histequalize()` function to enhance image contrast.
  - Applied histogram equalization to grayscale and RGB images and analyzed their effects.


- **Cryptography in Images**:
  - Extracted hidden messages from images using **LSB (Least Significant Bit) Steganography**.
  - Developed `crypt()` and `decrypt()` functions to embed and extract messages from images.
- **Linear Piece-wise Transformations**:
  - Applied transformations to enhance image contrast.
  - Analyzed pixel intensity variations before and after transformations.
- **Optimized Performance**: Used vectorized implementations for efficient processing of large images.

# 3. Advanced Image Processing: Filtering, Edge Detection, Denoising, and Transformation Techniques

## Overview
This project explores various **image processing techniques**, including **filtering, edge detection, noise removal, morphological operations, and image transformations** to enhance and analyze images. All functions are implemented from scratch using **NumPy, Matplotlib, and OpenCV (basic functions)** to gain a deep understanding of image manipulation.

## Features
### **1. 2D Convolution & Filtering**
- Implemented a custom **conv2D()** function for image convolution.
- Applied **Mean, Median, Gaussian, and Bilateral filters** for image smoothing and noise reduction.
- Optimized Mean Filtering using a **fastMeanFilter()** implementation.

### **2. Edge Detection**
- Implemented **Sobel, Prewitt, Roberts, and Laplacian filters** to detect image gradients.
- Plotted edge maps and analyzed different methods for detecting boundaries.


### **3. Image Sharpening**
- Developed an **Unsharp Masking** function to enhance fine details.
- Implemented a **High-Boost Filter** to amplify image features.
- Compared the effects of different sharpening techniques.

### **4. Noise Removal & Denoising**
- Analyzed different types of noise present in images.
- Applied **optimal filtering techniques** to restore corrupted images.
- Compared the efficiency of different noise removal methods.


### **5. Morphological Operations**
- Designed a pipeline to **separate overlapping objects (e.g., coins) using morphological transformations**.
- Used different structuring elements for segmentation and object detection.

### **6. Signature Verification**
- Skeletonized handwritten signatures using a custom function.
- Analyzed the stability of skeletons across different signatures from the **CEDAR dataset**.


### **7. Medical Image Enhancement**
- Processed **nuclear whole-body bone scans** to highlight skeletal structures.
- Applied sharpening techniques to enhance medical imaging details.

### **8. Image Restoration & Transformation**
- Used filtering and denoising techniques to recover corrupted images.
- Applied various transformations to improve image clarity and structure.


# 4. Fourier Transform, Image Enhancement, and Morphological Processing in Digital Image Processing

## Overview
This project explores **Fourier Transform-based analysis, image restoration, noise removal, and morphological processing** for enhancing and analyzing images. Implemented **DFT, FFT, IFFT, super-resolution, fingerprint recognition, and object detection** using **NumPy, OpenCV (basic functions), and Matplotlib**.

## Features

### **1. Fourier Transform Analysis**
- **1D & 2D Discrete Fourier Transform (DFT):** Implemented custom **dft1()** and **dft2()** functions without using OpenCV’s FFT functions.
- **Fast Fourier Transform (FFT):** Developed **fft1()** and **fft2()** to optimize Fourier Transform computations.
- **Frequency Spectrum Analysis:** Analyzed frequency components of an **audio signal (1.wav)** and generated a frequency vs. magnitude plot.
- **Time Complexity Analysis:** Compared execution time for different array sizes `[128, 256, 512, 1024]` to showcase FFT’s efficiency.
- **Fourier Transform on Images:** Applied **2D-DFT and 2D-FFT** on mathematical and real-world image signals.
- **Phase and Magnitude Spectrum Modifications:** Reconstructed images after swapping **phase/magnitude components**.

### **2. Image Restoration & Super-Resolution**
- **Fingerprint Enhancement:** Denoised smudged and noisy **fingerprint images** for better recognition.
- **Super-Resolution using Frequency Filters:** Applied **Low-Pass and High-Pass filtering** to enhance image clarity.

- **Noise Removal & Artifact Removal:** Processed images such as `bird.png` and `cart.jpg` to remove unwanted artifacts.

### **3. Morphological Operations & Object Detection**
- **Coin Counting:** Used **morphological transformations (erosion, dilation, opening, closing)** and thresholding to detect and count coins.

- **Skeletonization of Human Bone Structures:** Applied **skeletonization algorithms** to analyze **human bone structure in `human.png`**.

- **Fingerprint Recognition & Edge Detection:** Combined **morphological operations, Gabor filters, thresholding, and skeletonization** to enhance `fingerprint2.png` for accurate recognition.


# 5. Image Segmentation, Hough Transform, and Corner Detection in Digital Image Processing

## Overview
This project explores **image segmentation, Hough Transform for line and circle detection, and Harris Corner Detection** for feature extraction and analysis. It includes implementations of **thresholding techniques, edge detection, and corner detection** using **Python and OpenCV**, optimizing detection accuracy for real-world applications.

## Features

### **1. Image Segmentation**
- **Implemented Various Thresholding Techniques:**
  - **Binary Thresholding**
  - **Adaptive Thresholding**
  - **Otsu’s Thresholding**
- **Comparison and Analysis:**
  - Evaluated segmentation effectiveness by analyzing object boundaries and noise levels.
  - Displayed original vs. segmented images for clear comparison.

### **2. Hough Transform for Line and Circle Detection**
- **Hough Line Transform:**
  - Applied **Canny edge detection** before Hough Transform.
  - Detected straight lines in structured images such as roads, grids, and buildings.
  - Optimized line detection using different **threshold parameters**.

- **Hough Circle Transform:**
  - Applied preprocessing techniques like **smoothing** for improved circle detection.
  - Detected circular objects like **coins, wheels, and round signs**.
  - Experimented with **radius ranges and accumulator thresholds** for improved accuracy.

### **3. Harris Corner Detection**
- **Corner Detection Implementation:**
  - Developed a **Harris Corner Detection function** to identify distinct corners in an image.
  - Applied corner detection to structured images like **chessboards and buildings**.
  - Marked detected corners on images for better visualization.
- **Optimization and Parameter Tuning:**
  - Experimented with the sensitivity parameter **(k-value)**.
  - Observed effects of different k-values on feature detection.

### **4. Performance Analysis and Optimization**
- Compared **segmentation and feature detection** results using different preprocessing techniques.
- Adjusted **threshold parameters, radius ranges, and accumulator thresholds** to improve detection accuracy.