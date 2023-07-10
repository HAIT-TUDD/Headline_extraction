# Recognize_headlines

## Documentation

This is an example of a workflow to extract headlines in the "nationasozialistische" newspaper "Freiheitskampf" using the tool [LayoutParser](https://github.com/Layout-Parser/layout-parser). The extraction of headlines should be used to find manually annotated articles by HAIT researchers in the daily newspaper faster. Furthermore, a quantitative analysis could be performed in terms of size and wording of the headlines. This could give conclusions about the propagandistic effect of certain articles. The headline extraction will be complemented by a subsequent OCR processing. 


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

## Usage

Im Ordner "Example_notebooks" befinden sich weitere Erklärung zur Benutztung des Tools und ein Beispiel Workflow. It explains once how to extract the headlines with a self-trained model and then perform OCR recognition using Tesserocr. 


## Training 

The folder "Train_LayoutParser" contains explanations and instructions for annotating your own data. In addition, there is also an example notebook on which a training workflow was carried out with the help of Google Colab.


