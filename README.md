# Parallel_SFM
This repository contains a parallel implementation of Parallel SFM

### Requirements
1. Python 3.5
2. OpenCV 3.4.2.16
3. jupyter notebook
4. Pycuda

### Installing

Inorder to install the requirements, 
pip install -r requirements.txt

You will need to run 
1. SFM_CPU_Version on your local jupyter notebook
2. SFM_GPU_Version on google collaboratory. 

Before Running the ipynb file, please setup the data on your drive:
1. Upload the "data" folder to your google drive.
2. In the google notebook, you will be mounting your drive.
3. In the main function, please setup the paths for the input images and instrinsic params:
```
img_pattern = 'drive/My Drive/data/folder1/*.ppm' 
intrinsic = intrinsic_reader('drive/My Drive/data/folder1/intrinsics.txt') # Retrieve intrinsic parameters
```
4. An "Output" folder is created inside the "data" folder and the following path is set to save outputs obj files:
```
output_dir = 'drive/My Drive/data/Output' # Folder to save output results
```


### data Directory Layout

```
└── data
    ├── folder1
    │      ├── rdimage.000.ppm
    │      ├── rdimage.001.ppm
    │      ├── rdimage.002.ppm
    │      └── intrinsics.txt
    ├── folder2
    │      ├── 01.jpg
    │      ├── 02.jpg
    │      ├── 03.jpg
    │      ├── dataset_files.txt
    │      ├── intrinsics.txt 
    │      └── params.txt
    └── Output
```

### Authors

The serial version is borrowed from [Pranav Kadam's](https://github.com/pranavkdm) SfM Implementation. 
This code has been extended to the parallel version by:

* **Anirudh Kulkarni** - [KulkarniAnirudh26](https://github.com/KulkarniAnirudh26)
* **Anand Ravi** - [anandravi24](https://github.com/anandravi24)
* **Siddhant Nadkarni** - [SiddhantNadkarni](https://github.com/SiddhantNadkarni)
