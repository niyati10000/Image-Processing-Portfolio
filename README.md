Project Overview
This repository is a comprehensive technical showcase of Digital Image Processing (DIP) algorithms implemented from first principles. The project is structured into five modules, progressing from foundational pixel-level manipulations to advanced frequency domain transforms and video sequence analysis. The primary objective is to demonstrate the mathematical logic and practical application of image enhancement, restoration, and feature extraction.

Repository Structure
The project is organized into modular directories, each containing localized documentation, source code, and relevant datasets:

Module 1: Spatial Domain Intensity Transformations

Foundational mapping of pixel intensities.

Module 2: Image Enhancement and Filtering

Spatial domain noise reduction and sharpening.

Module 3: Frequency Domain Analysis

Fourier and Cosine transform implementations.

Module 4: Morphological Image Processing

Shape-based analysis and structural correction.

Module 5: Segmentation and Video Analysis

Object isolation and time-series data handling.

Technical Implementation Details

Module 1: Spatial Transformations
Focuses on the manipulation of the image dynamic range and contrast using point-processing techniques.

Digital Negative: Implements intensity inversion where s = L - 1 - r, used for enhancing details in dark regions.
Contrast Stretching: Utilizes piecewise linear functions to expand the gray-level range of an image
Power-Law (Gamma) Transformation: Implements s = c . r^{\gamma} with mandatory pixel normalization to the [0, 1] range to ensure mathematical stability.

Module 2: Spatial Filtering
Addresses image quality improvement through neighborhood operations.

Histogram Equalization: Enhances global contrast by linearizing the cumulative distribution function (CDF) of pixel intensities.
Smoothing: Employs Averaging kernels (low-pass filters) to attenuate high-frequency noise.
Edge Detection: Implements first-order (Sobel, Prewitt) and second-order (Laplacian) derivative operators for structural feature extraction.

Module 3: Frequency Domain Analysis
Transitions image data from spatial coordinates to frequency components.

2D Discrete Fourier Transform (DFT): Decomposes images into sinusoidal components.
Discrete Cosine Transform (DCT): Demonstrates energy compaction properties, essential for standards such as JPEG.
Visualization: Employs logarithmic scaling (20.log(1 + |F|)) to visualize the wide dynamic range of frequency spectra.


Module 4: Morphological Operations
Applies set-theory-based operations to binary image structures.

Dilation & Erosion: Fundamental operations for expanding or contracting object boundaries.
Opening & Closing: Strategic combinations used for noise suppression (Opening) and filling structural gaps (Closing).
Polarity Fix: Implements bitwise inversion to ensure processing of white objects on black backgrounds

Module 5: Segmentation & Video Processing
Concludes with automated image analysis and temporal data handling.

Otsu’s Method: An automated thresholding algorithm that maximizes inter-class variance to isolate foreground objects.
Video Processing: Demonstrates frame extraction and the sequential application of spatial filters to video streams.
