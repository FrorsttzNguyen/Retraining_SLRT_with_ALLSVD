# Developing and Retraining the ASLLVD Dataset for Transformer-based Sign Language Recognition and Translation (CVPR 2020)

This repo contains the training and evaluation code for the paper [Sign Language Transformers: Sign Language Transformers: Joint End-to-end Sign Language Recognition and Translation](https://www.cihancamgoz.com/pub/camgoz2020cvpr.pdf). 

This code is based on [Joey NMT](https://github.com/joeynmt/joeynmt) but modified to realize joint continuous sign language recognition and translation. For text-to-text translation experiments, you can use the original Joey NMT framework.

## Description
In this project, I developed and retrained the ASLLVD dataset for sign language recognition and translation using Transformer-based models. The key steps in the process include:

- **Data Access and Annotation Extraction**: Accessed the ASLLVD dataset annotations to identify and extract relevant video data from the [Dai ASLLVD Glossing with Variations](http://www.bu.edu/asllrp/dai-asllvd-BU_glossing_with_variations_HS_information-extended-urls-RU.xlsx).

- **Video Cutting**: Utilized the start and end times from the annotations to cut the videos into segments that correspond to specific sign language samples.


- **Feature Extraction**: Employed the R(2+1)D model to extract features from the segmented videos and compressed these features into .train files for subsequent model training.

- **Model Training**: Implemented the training process using the modified code based on [Joey NMT](https://github.com/joeynmt/joeynmt) to achieve joint continuous sign language recognition and translation.
 
 
## Requirements
* Download the feature files using the `data/download.sh` script for training or using the `data/allsvd.train`

* [Optional] Create a conda or python virtual environment.

* Install required packages using the `requirements.txt` file.

    `pip install -r requirements.txt`

## Usage

  `python -m signjoey train configs/sign.yaml` 

! Note that the default data directory is `./data`. If you download them to somewhere else, you need to update the `data_path` parameters in your config file.   
## ToDo:

- [X] *Initial code release.*
- [X] *Release image features for Phoenix2014T.*
- [ ] Share extensive qualitative and quantitative results & config files to generate them.
- [ ] (Nice to have) - Guide to set up conda environment and docker image.
