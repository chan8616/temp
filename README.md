# Video classification using audio-only features

## How to run
### 1. Unzip code.zip
#### Directory may look like this:
####	code
#####	>> train_model.py
#####	>> extract_result.py
#####	>> soundnet.conv7.mlp.model
#####	>> X_train.pkl
#####	>> y_train.pkl
#####	>> X_test.pkl
#####	>> y_test.pkl

### 2. To Train a model with conv7 features from SoundNet:
###    (train/validation sets are already seperated. Just use .pkl files.)
'''
	python train_mlp.py ./X_train_pkl ./y_train_pkl ./X_test.pkl ./y_test.pkl soundnet.conv7.mlp.model
'''
### 3. Extract the validation result(Confusion matrix)
'''
	python extract_result.py ./soundnet.conv7.mlp.model ./X_test.pkl ./y_test.pkl ./confusion_matrix.png
'''
