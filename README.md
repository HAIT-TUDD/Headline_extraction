# Recognize_headlines

## Documentation

## Installation

First of all you need to create a virtual environment for python. You can also follow the instructions without a virtual environment, but that is not recommended.

```
python3.7 -m venv "name of your virtual environment"
source name_of_env/bin/activate 	#with this command you can activate the environment

#if you want to deactivate the environment just type:
deactivate 
#but for the installation process you need to be in the active environment

```

Second we need to install the packages for Layoutparser:

```

pip install layoutparser	#will install the base LayoutParser library (layout data structure and visualization, Load/export the layout data)
pip install torchvision && pip install "detectron2@git+https://github.com/facebookresearch/detectron2.git@v0.5#egg=detectron2"	#will install detectron2, which is needed to create a detection model with self trained data

```

Third we need to install an OCR Processor. For this task i chose Tesserocr.
For Tesserocr you need to install some Prerequisites. See [here](https://github.com/sirfz/tesserocr) 

```
sudo apt-get install tesseract-ocr libtesseract-dev libleptonica-dev pkg-config
 pip install tesserocr

```

## Training 

## Usage
