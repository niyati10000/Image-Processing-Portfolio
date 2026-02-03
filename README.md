# Digital Image Processing (DIP) Fundamentals

## Project Overview
This repository serves as a comprehensive technical showcase of Digital Image Processing (DIP) algorithms implemented from first principles. The project is structured into five distinct modules, progressing from foundational pixel-level manipulations to advanced frequency domain transforms and video sequence analysis.

The primary objective of this codebase is to demonstrate the mathematical logic and practical application of image enhancement, restoration, feature extraction, and segmentation without reliance on high-level black-box API calls.

## Repository Architecture

The project is organized into modular directories, each containing localized documentation, source code, and relevant datasets.

### Module 1: Spatial Domain Intensity Transformations
Focuses on the manipulation of the image dynamic range and contrast using point-processing techniques.
* **Digital Negative:** Implements intensity inversion (`s = L - 1 - r`), primarily used for enhancing white or gray details embedded in dark regions of an image.
* **Contrast Stretching:** Utilizes piecewise linear functions to expand the dynamic range of an image's gray levels.
* **Power-Law (Gamma) Transformation:** Implements the formula `s = c * r^γ` with mandatory pixel normalization to the [0, 1] range to ensure mathematical stability and correct luminance correction.

### Module 2: Image Enhancement and Filtering
Addresses image quality improvement through spatial neighborhood operations.
* **Histogram Equalization:** Enhances global contrast by linearizing the cumulative distribution function (CDF) of pixel intensities.
* **Spatial Smoothing:** Employs Averaging kernels (low-pass filters) to attenuate high-frequency noise.
* **Edge Detection:** Implements first-order (Sobel, Prewitt) and second-order (Laplacian) derivative operators for structural feature extraction.

### Module 3: Frequency Domain Analysis
Transitions image data from spatial coordinates to frequency components.
* **2D Discrete Fourier Transform (DFT):** Decomposes images into sinusoidal components to analyze frequency content.
* **Discrete Cosine Transform (DCT):** Demonstrates energy compaction properties, essential for compression standards such as JPEG.
* **Spectrum Visualization:** Employs logarithmic scaling (`20 * log(1 + |F|)`) to properly visualize the wide dynamic range of frequency spectra.

### Module 4: Morphological Image Processing
Applies set-theory-based operations to binary image structures.
* **Dilation & Erosion:** Fundamental operations for expanding or contracting object boundaries.
* **Opening & Closing:** Strategic combinations of dilation and erosion used for noise suppression (Opening) and filling structural gaps (Closing).
* **Polarity Management:** Implements bitwise inversion to ensure consistent processing of white objects on black backgrounds.

### Module 5: Segmentation and Video Analysis
Concludes with automated image analysis and temporal data handling.
* **Otsu’s Method:** An automated global thresholding algorithm that maximizes inter-class variance to isolate foreground objects from the background.
* **Video Processing:** Demonstrates frame extraction logic and the sequential application of spatial filters to video streams.

## Technical Requirements
To run the modules in this repository, the following dependencies are required:

* Python 3.x
* OpenCV (`cv2`)
* NumPy
* Matplotlib (for visualization)

## Setup and Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/dip-algorithms.git](https://github.com/your-username/dip-algorithms.git)
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd dip-algorithms
    ```
3.  **Run specific modules:**
    Navigate to the specific module folder and execute the Python scripts to view the processing outputs.

## License
This project is open-source and available for educational and research purposes.
