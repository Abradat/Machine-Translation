# Machine-Translation
Machine Translation project for NLP course. Subject of this project is translating English movie subtitles to persian movie subtitles.

## Overview
This program uses OpenNMT for training data and machine translation

## OpenNMT
After downloading the project you need to set the GOPATH variable to the root of your project.

```git clone https://github.com/OpenNMT/OpenNMT-py```
```cd OpenNMT-py```
```pip3 install -r requirements.txt```

## Preprocessing Data

```python3 preprocess.py -train_src data/en-train.txt -train_tgt data/fa-train.txt -valid_src data/en-val.txt -valid_tgt data/fa-val.txt -save_data data/demo```

## Training the model

```python3 train.py -data data/demo -save_model demo-model```

## Testing

```python3 translate.py -model demo-model_XYZ.pt -src data/en-test.txt -output pred.txt -replace_unk -verbose```

