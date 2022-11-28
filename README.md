# NN_for_cell_culture
Code from the paper "Objectivization of virus titration method in GMP-regulated environment using artificial intelligence-based classification system", doi: https://doi.org/10.1016/j.ejpb.2022.11.020.

Full text here:
https://authors.elsevier.com/a/1g8uU_LNMvXu9N

and here:
https://drive.google.com/file/d/10ryDq3-WJZHTqd6XYKq-00IwF_nlgaqL/view?usp=sharing

AI-based objectivization/automatization of cell culture-based virus titration methods.
This project is used to validate AI-based classification of microscope-acquired images of an analytical virus titration assay against readings of a human operator. This simple binary neural network classifier is built from several convolutional and pooling layers with a binary classifier at the output. The classifier is trained on number of test images pre-classified by human expert readers. 
There are three tested cell-culture systems:
1. Vero cells in suspension infected with Newcastle disease virus
2. Primary chicken embryo kidney cells infected with infectious bronchitis virus
3. Chicken embryo fibroblasts infected with infectious bursal disease virus

Neural network is a binary classifier which outputs probability of a particular image representing "positive" (i.e. infected) cell culture well.

## Preprocessing:
1. Original imagese 1280 x 720
2. Converted to grayscale (offline)
3. Extract center 500x500 square

## Postprocessing
In order to provide an insight into the neural network’s choice of discriminative features used for classifications of images, Gradient-weighted Class Activation Mapping (Grad-CAM) was used to generate activation maps of images from the dataset. The heatmaps for selected images were generated using tf-explain library (see manuscript for references and details).

## Examples of non-infected and virus-infected images used for assay validation
Examples of negative (non-infected) and positive (virus infected) wells from the validation assays. 96-well cell culture plates were seeded with either Vero, CEF or CEK cells and infected with 10-fold serial dilutions of NDV, IBDV or IBV viruses respectively. Wells were examined 5-7 days later under 100-200 fold magnification for CPE and classified as negative (no CPE visible) or positive (visible CPE). Cell well images were subjected to Grad-CAM analysis to highlight regions most relevant for trained neural network’s prediction outcome.

![guthubimg](https://user-images.githubusercontent.com/98668610/204270497-e8e70382-1538-4b05-89ef-262373220684.png)

