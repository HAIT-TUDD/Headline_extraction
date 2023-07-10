# How to use

In this folder you will see how to use LayoutParser with a self-trained model and Tesserocr to extract and OCR titles from the "Freiheitskampf" newspaper.

## Notebooks

#### "Example_Usage"

The "Example_Usage" notebook explains how to select the right options for the layout parser and how to use an OCR algorithm. 
To use the notebook, you need to download some newspaper pages that you want to edit. Then you need to edit the path to the folder that contains the newspaper pages.

The trained data for the layout parser can be found in "../Train_LayoutParser/". There you will find instructions on how to perform the training.
In the Example Notebook we use tesserocr for Optical Character Recognition. 

#### "Download_relevant_pages"

Here you can find a script to extract the Freiheitskampf pages where manually annotated articles were read by researchers. Also the titles of the manually annotated articles included in the database have been extracted.

## Train LayoutParser

See "../Train_Layoutparser/" for further Information.

## OCR 

Especially the OCR step can be modified in an extremely wide range. It would be possible to use another OCR tool (e.g. Calamari), preprocess the images and perform binarization, deskewing, dewarping, denoising, etc., or even train a custom model for the Freiheitskampf fonts. 

There is a large list of models available for Tesserocr: 
[https://github.com/tesseract-ocr/tessdata](https://github.com/tesseract-ocr/tessdata)

or take a look at the OCR-D documentation for more models:
[https://ocr-d.de/en/workflows#step-14-text-recognition](https://ocr-d.de/en/workflows#step-14-text-recognition)

For this task, I chose Tesserocr rather than Calamari because Calamari is trained to recognize single lines. But since the layout paser usually recognizes a title with its associated subtitle, it is not possible to use Calamari. What you can do is to split the recognized headings into title and subtitle. 
