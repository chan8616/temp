# Multimodal fusion for MED
---------------------------------------------------
## How to run
1. Unzip the download file <br />
2. Run the command below: <br />
``` python
python hw2.py
``` 
3. Details of the architectures
I've tried several architectures like MobileNet and ConvNext.
But my best architecture looks like this:
```bash
├── Stage configuration
│   ├── [6,  24, 2, 2]
│   ├── [6,  40, 3, 2]
│   ├── [6,  80, 3, 2]
│   ├── [6,  112, 2, 1]
│   ├── [6, 160, 3, 2]
│   └── [6, 960, 3, 1]
├── Activation function = GELU
├── Data augmentation
│   ├── ttf.RandAugment()
│   ├── ttf.ToTensor()
│   ├── ttf.Normalize(mean=[0.5131001, 0.4034442, 0.35218757], std=[0.2706944, 0.23636194, 0.2226286])
                     (mean and std are calculated from the dataset) 
```
