# Video classification using audio-only features
---------------------------------------------------
## How to run
1. Unzip code.zip /n
   Please place all unziped files under 11775-hws/spring2022/hw1. /n
   I assume that you have Soundnet conv7 features under 11775-hws/spring2022/hw1/soundnet/avg_pooling/conv7. /n
   Directory may look like this: /n
```bash
├── code
│   ├── split_dataset.py
│   ├── train_model.py
│   ├── extract_result.py
│   ├── soundnet.conv7.mlp.model
│   ├── X_train.pkl
│   ├── y_train.pkl
│   ├── X_test.pkl
│   └── y_test.pkl
```
2. Split dataset into train/validation using conv7 features from SoundNet:
(train/validation sets are already seperated. Just use .pkl files.)
``` python
python split_dataset.py ./soundnet/avg_pooling/conv7 1024 labels/train_val.csv
```
3. To Train a model with conv7 features from SoundNet:
(you should have train/validation pickle files which are already seperated from the original dataset.)
``` python
python train_mlp.py ./X_train_pkl ./y_train_pkl ./X_test.pkl ./y_test.pkl soundnet.conv7.mlp.model
```
4. Extract the validation result(Confusion matrix)
``` python
python extract_result.py ./soundnet.conv7.mlp.model ./X_test.pkl ./y_test.pkl ./confusion_matrix.png
```
