# ARTI 403 — Image Processing

Lab work for **ARTI 403 – Image Processing**
College of Computer Science and Information Technology — Department of Computer Engineering
Imam Abdulrahman Bin Faisal University — 2026 / 2027

| | |
|---|---|
| **Student name** | *Abdulrahman Saleh Alaamri* |
| **Student ID** | *2240002427* |
| **Section** | *Computer Engineering* |
| **Instructor** | *Dr. Aftab Khan* |

This is the single repository used for the whole course, as required by the student guidelines.
One folder is added per lab session, and every lab is delivered as a Jupyter notebook that is
committed **with its outputs already executed**, so it can be read without running anything.

## Repository structure

```
ARTI403/
├── README.md
├── requirements.txt
├── images/                                  # test images shared by all labs
│   ├── lena_gray_256.tif                    #   256x256, 8-bit gray
│   ├── cameraman.tif                        #   256x256, 8-bit gray
│   ├── A.png                                #   binary set A (disk)
│   └── B.png                                #   binary set B (square)
├── Lab1/
│   ├── Lab1_Basics_of_Programming_with_Python.ipynb
│   ├── Lab1_Basics_of_Programming_with_Python.pdf   # PDF report of the notebook
│   └── output/                              # images written by the notebook
├── Lab2/
│   ├── Lab2_Digital_Image_Fundamentals.ipynb
│   ├── Lab2_Digital_Image_Fundamentals.pdf
│   └── output/                              # images written by the notebook
├── Lab3/  ...  Lab5/                        # notebook, PDF report and output/ folder
├── Lab6/  ...  Lab10/                       # one folder per remaining session
└── ...
```

Every delivered lab folder also has a PDF export of its notebook (the report for Blackboard).
The folders of the labs that have not been delivered yet contain only a placeholder
`README.md`; the notebook and its `output/` folder are added when the lab is done.

## Labs

| Lab | Topic | Notebook | Contents |
|-----|-------|----------|----------|
| 1 | Basics of programming with Python | [Lab1_Basics_of_Programming_with_Python.ipynb](Lab1/Lab1_Basics_of_Programming_with_Python.ipynb) | Environment setup; Python & NumPy cheat-sheet exercises; loading and visualizing images with OpenCV and PIL; storing images; displaying an image as an array; NumPy operations on the image array |
| 2 | Digital image fundamentals | [Lab2_Digital_Image_Fundamentals.ipynb](Lab2/Lab2_Digital_Image_Fundamentals.ipynb) | Sampling and quantization; arithmetic operations; sets and logical operations; **Task 1** effect of the sampling and quantization parameters; **Task 2** subtraction, adding a constant of 175, set difference, symmetric difference and intersection |
| 3 | Image manipulations using OpenCV | [Lab3_Image_Manipulations_using_OpenCV.ipynb](Lab3/Lab3_Image_Manipulations_using_OpenCV.ipynb) | **Task 1** geometric transformations: resize, rotation by 120°, shear; **Task 2** intensity transformations: negative, log, power law |
| 4 | Intensity transformations and filtering (spatial domain) | [Lab4_Intensity_Transformations_and_Filtering.ipynb](Lab4/Lab4_Intensity_Transformations_and_Filtering.ipynb) | Thresholding; contrast stretching and histograms of the moon image; **Task 1** rescaling between the 3rd and 80th percentiles; **Task 2** histogram equalization; **Task 3** histogram matching (Chelsea to rocket) |
| 5 | Spatial filtering: smoothing and sharpening | [Lab5_Spatial_Filtering_Smoothing_and_Sharpening.ipynb](Lab5/Lab5_Spatial_Filtering_Smoothing_and_Sharpening.ipynb) | Unsharp masking; **Task 1** 7x7 box filter; **Task 2** 5x5 and 21x21 Gaussian filters; **Task 3** 3x3 Laplacian sharpening |
| 6 | *to be announced* | [Lab6/](Lab6/) | not delivered yet |
| 7 | *to be announced* | [Lab7/](Lab7/) | not delivered yet |
| 8 | *to be announced* | [Lab8/](Lab8/) | not delivered yet |
| 9 | *to be announced* | [Lab9/](Lab9/) | not delivered yet |
| 10 | *to be announced* | [Lab10/](Lab10/) | not delivered yet |

## Requirements

* Python 3 (Anaconda distribution)
* NumPy, OpenCV, Pillow, Matplotlib, SciPy, scikit-image

```bash
# with conda (Anaconda / Miniconda)
conda install -c conda-forge numpy opencv pillow matplotlib scipy scikit-image jupyter

# or with pip
pip install -r requirements.txt
```

## How to run

```bash
git clone <this-repository-url>
cd ARTI403
jupyter notebook
```

Then open the notebook of the lab and run the cells from top to bottom
(*Kernel → Restart & Run All*).

The notebooks are meant to be started **from inside their own lab folder**, since the images are
referenced relatively as `../images/...`. Opening them from the Jupyter file browser does this
automatically.

## Notes on the test images

* `lena_gray_256.tif` and `cameraman.tif` are the two standard test images used by the lab manuals,
  both 256 × 256 pixels and 8-bit gray-scale.
* `Parrot.png`, used by the Lab 4 and Lab 5 manuals, is not in the repo. Lab 4 uses `cameraman.tif` instead, and
  Lab 5 uses the `chelsea` image from scikit-image. Lab 4 also uses the `moon`, `rocket` and `chelsea` images of
  scikit-image, which are saved in `Lab4/output/`.
* `A.png` and `B.png` are two binary images (values 0 and 255) representing two overlapping sets —
  a disk **A** and a square **B** — used for the logical and set operations of Lab 2.
