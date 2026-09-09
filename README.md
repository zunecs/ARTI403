# ARTI 403 — Image Processing

Lab work for **ARTI 403 – Image Processing**
College of Computer Science and Information Technology — Department of Computer Engineering
Imam Abdulrahman Bin Faisal University — 2026 / 2027

| | |
|---|---|
| **Student name** | *&lt;write your name here&gt;* |
| **Student ID** | *&lt;write your ID here&gt;* |
| **Section** | *&lt;write your section here&gt;* |
| **Instructor** | *&lt;write your instructor's name here&gt;* |

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
│   └── output/                              # images written by the notebook
└── Lab2/
    ├── Lab2_Digital_Image_Fundamentals.ipynb
    └── output/                              # images written by the notebook
```

## Labs

| Lab | Topic | Notebook | Contents |
|-----|-------|----------|----------|
| 1 | Basics of programming with Python | [Lab1_Basics_of_Programming_with_Python.ipynb](Lab1/Lab1_Basics_of_Programming_with_Python.ipynb) | Environment setup; Python & NumPy cheat-sheet exercises; loading and visualizing images with OpenCV and PIL; storing images; displaying an image as an array; NumPy operations on the image array |
| 2 | Digital image fundamentals | [Lab2_Digital_Image_Fundamentals.ipynb](Lab2/Lab2_Digital_Image_Fundamentals.ipynb) | Sampling and quantization; arithmetic operations; sets and logical operations; **Task 1** effect of the sampling and quantization parameters; **Task 2** subtraction, adding a constant of 175, set difference, symmetric difference and intersection |

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
* `A.png` and `B.png` are two binary images (values 0 and 255) representing two overlapping sets —
  a disk **A** and a square **B** — used for the logical and set operations of Lab 2.
