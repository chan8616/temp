# Video classification using audio-only features
---------------------------------------------------
## How to run
1. Unzip code.zip <br />
   Please place all unziped files under 11775-hws/spring2022/hw2. <br />
   I assume that you have convolution features from the last convolution layer of VGG19 <br />
   Directory may look like this: <br />
```bash
├── code
│   ├── modules
│   ├── stages
│   ├── run_bow.py
│   ├── run_cnn.py
│   ├── run_mlp.py
│   ├── run_sift.py
│   └── train_kmeans
```
2. Run run_cnn.py to extract CNN features:<br />
``` python
python 
python code/run_cnn.py data/labels/train_val.csv
python code/run_cnn.py data/labels/test_for_students.csv
python code/run_cnn.py data/labels_p2/test_for_students.csv
```
3. To Train and test a MLP model with conv features:<br />
``` python
python code/run_mlp.py cnn --feature_dir data/cnn --num_features 512
```
