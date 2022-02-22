# NN_for_cell_culture
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

Examples of processed images used for training:

## CEK (positive), Vero (positive): 


![Image000010](https://user-images.githubusercontent.com/98668610/154979860-87ff9a2b-6894-44a2-a8b4-d0723bbb86a4.jpg)     ![WIN_20220214_07_29_20_Pro](https://user-images.githubusercontent.com/98668610/155065058-f51a25a2-dfa1-43de-a184-b49640849c13.jpg)


## CEK (negative), Vero (negative):

![Image000065](https://user-images.githubusercontent.com/98668610/154979994-5eea7ce6-3727-4e41-bbac-b6a3d28979f2.jpg)      ![WIN_20220214_10_35_49_Pro](https://user-images.githubusercontent.com/98668610/155065437-b25dc9f0-61e1-4baf-a14f-6e1e1d061687.jpg)

