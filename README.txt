Deep Learning-Based Object Detection in High-Altitude Thermal Imagery from UAVs
============================================================================

This repository contains the results and documentation of a graduation project 
on object detection in thermal UAV imagery using the HIT-UAV dataset. 
The base model is YOLOv8, and different attention modules (CBAM, CoordAtt) 
were tested together with preprocessing techniques such as CLAHE.

⚠️ Important Note
-----------------
The repository mainly provides the dataset structure, experimental results, 
and documentation. While the specific YAML configurations for the tested 
attention modules (CBAM, CoordAtt) are not included, researchers can reproduce 
similar experiments by **integrating their own attention mechanisms into YOLOv8m** 
and training the model using the provided data structure and pipeline.

The Python scripts in `src/` are simplified versions that show the basic workflow 
and can serve as a reference, but do not fully replicate the original experiments.


Repository Structure
--------------------

uav-thermal-object-detection/
│── data/
│   ├── images/             -> Training and test images (thermal UAV)
│   └── labels/             -> Corresponding YOLO-format labels
│
│── results/
│   ├── train_cbam_clahe/   -> Training results with YOLOv8 + CBAM + CLAHE
│   ├── test_coordatt/      -> Test results with YOLOv8 + CoordAtt
│   └── test_clahe/         -> Training results with YOLOv8 + CLAHE
│
│── docs/
│   ├── project_poster.pdf          -> Poster prepared for project presentation
│   └── project_report.pdf          -> Detailed project report
│
│── src/
│   └── project.ipynb       -> Notebook for data preparation and baseline experiments
│
│── README.txt              -> Project documentation (this file)



Results
-------

Results are available under the "results/" folder:

- YOLOv8 + CBAM + CLAHE:
  test_cbam_clahe/

- YOLOv8 + CoordAtt:
  test_coordatt/

- YOLOv8 + CLAHE:
  test_clahe/

Each folder contains metrics (mAP, precision, recall, loss curves) and test outputs.

Example detection outputs can be added here for clarity.


Documentation
-------------

- Poster  -> docs/project_poster.pdf
- Report  -> docs/project_report.pdf

Both documents explain methodology, dataset details, and obtained results.


Technologies Used
-----------------

- Ultralytics YOLOv8
- PyTorch
- OpenCV (CLAHE preprocessing)
- Python 3.10+


Notes
-----

- Dataset is not included due to size; please download HIT-UAV dataset separately 
  and place it under:
  data/images
  data/labels

- Results provided are based on experiments conducted in June 2025.

- This repository serves as a **research archive** for results and documentation.
  The provided scripts illustrate the workflow and can be adapted to new attention
  modules integrated into YOLOv8m for further experiments.

