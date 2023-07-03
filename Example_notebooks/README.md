# How to use

In this folder you can see how to use the LayoutParser with a self trained Model, and Tesserocr to extract and OCR Titles from the Freiheitskampf Newspaper


## Notebooks

#### "Example_Usage"

In the Notebook "Example_Usage" you can find an explained Notebook how to select the right options for Layoutparser, and how to use an OCR Algorithm. 
To use the notebook you need to download some Newspaper pages you want to process. Then you need to edit the path to the folder containing the newspaper pages.

The trained data for Layoutparser can be found in "../Train_LayoutParser/". There you can find a instructions how to do the training.
In the Example Notebook we use tesserocr for the Optical Character Recognition. 

#### "Download_relevant_pages"

Here you can find a script, where you can extract the pages of Freiheitskampf where manually annotated Articles were read from the researchers. Also the titles from the manually annotated Articles, which are included in the database, were extracted and 

## Train LayoutParser

See "../Train_Layoutparser/" for further Information.

## OCR 

Especially the OCR step can be modified in a extremly wide range. It would be possible to use another OCR Tool (e.g. Calamari), to preprocess the images an do binarization, deskewing, dewarping, denoising etc. or even to train a own model for the fonts of "Freiheitskampf". 

There is a big list of models available for Tesserocr: 
[https://github.com/tesseract-ocr/tessdata](https://github.com/tesseract-ocr/tessdata)

or have a look at the OCR-D Documentation for further models:
[https://ocr-d.de/en/workflows#step-14-text-recognition](https://ocr-d.de/en/workflows#step-14-text-recognition)

For this task i choose Tesserocr and not Calamari because Calamari is trained on single line detections. But since Layoutpaser recognizes a title most of the time with the related subtitle it is not possible to use Calamari. What you can do is to split the detected headlines in Title and Subtitle. 

