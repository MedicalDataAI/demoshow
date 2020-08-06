# ThyroidUS AI
AI code demo, paper name
Lymph node metastasis prediction from primary breast cancer ultrasound images using deep learning

If you use this code in your research, consider citing:
```
@article{
  title={xxxx},
  author={xxxx},
  journal={xxxx},
  year={xxxx},
  publisher={xxxx}
}
```

## Prerequisites

- Ubuntu 18.04 with Nivida 2080Ti
- Python 3.6 with dependencies listed in the `requirements.txt` file
```
sudo pip install -r requirements.txt
```

## Running

1. clone the repo to local directory
```Bash
   git clone https://github.com/MedicalDataAI/demoshow.git
```

2. download the weight file of the trained model into the folder of "./models"
```Bash
   wget 'https://drive.google.com/file/d/1KWAmU7hbp-byJ9tM8Mh6_I9_85mOTYsD/view?usp=sharing'
```

4. use the trained model to predict the data of Clinical, BMUS, CDFI (NOTE: to replace the parameter of path with proper location of model file)

- Predict clinical data (NOTE: to replace the data in "./data/clinical.csv") into "./res/result_clinical.csv"
```Bash
   python3 clinical_lr.py
```   

- Predict BMUS data (NOTE: to replace the images in "./data/bmus/*") into "./res/result_bmus.csv"
```Bash
   python3 bmus_cnn.py
```

- Predict CDFI data (NOTE: to replace the images in "./data/cdfi/*") into "./res/result_cdfi.csv"
```Bash
   python3 cdfi_cnn.py
```

- Predict ensemble data (Prompt for input the risk of Clinical, BMUS and CDFI from clinical_lr.py, bmus_cnn.py and cdfi_cnn.py.)
```Bash
   python3 ensemble_bagging.py
```

