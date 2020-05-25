# nnfl_project_34
Neural Networks and Fuzzy Logic Group Project ID 34 : Keras Implementation of the research paper - Attention U-Net : Learning where to look for the pancreas


#SETUP -<br/>
Download the AttentionUNetImplementation.ipynb, Go to GOOGLE COLAB, and Open this Notebook.<br/>
Please run the notebook in COLAB ONLY. <br/>
Instructions to run are noted in it.<br/><br/>
Please make sure you run the project on GPU. In COLAB, you can change the virtual machine alloted to you by Runtime -> Change Runtime <br/>Type ->GPU as Hardware Accelerator<br/>


#DATASET<br/>
Dataset Used- Kaggle Ultrasound Nerve Segmentation https://www.kaggle.com/c/ultrasound-nerve-segmentation<br/><br/>
Make sure you create new API Token before running the notebook.<br/>
Go to Kaggle website -> My account -> Create New API Token and download the generated kaggle.json file. Upload when asked to choose files into colab<br/>


#ATTENTION UNET ARCHITECTURE <br/>

![Screenshot (188)](https://user-images.githubusercontent.com/37960440/82831420-06a6b500-9ed6-11ea-8f8e-314f9702c036.png) <br/>
Schematic Representation of Attention Unet <br/>

![AttentionUNetModel](https://user-images.githubusercontent.com/37960440/82830895-92b7dd00-9ed4-11ea-83ff-2bd95af131dc.png) <br/>
Model Architecture <br/>

![Attention_Gate](https://user-images.githubusercontent.com/37960440/82830928-a7947080-9ed4-11ea-9f80-58390424213f.png) <br/>
Attention Gates <br/>

Encoder Bottleneck Decoder Network<br/>
Attention U-Net aims to automatically learn to focus on target structures of varying shapes and sizes.Attention is used to perform class-specific pooling, which results in a more accurate and robust image classification performance. These attention maps can amplify the relevant regions, thus demonstrating superior generalisation over several benchmark datasets.<br/>
Attention U-Net aims to increase segmentation accuracy further and to work with fewer training samples, by attaching attention gates on top of the standard U-Net.<br/>
It eliminates the necessity of an external object localisation model which some segmentation architecture needs, thus improving the model sensitivity and accuracy to foreground pixels without significant computation overhead.<br/>
It also incorporates grid-based gating, which allows attention coefficients to be more specific to local regions.<br/>

#SOFT_DICE_COEFF_LOSS, DICE_COEFF_METRICS<br/>
Kaggle competitions as well as the paper uses DSC(Dice Coefficient) to evaluate the performance of the model.<br/>
Soft Dice Coefficient Loss is used for better training of the Neural network. <br/>

#OPTIMISER<br/>
Adam Optimiser(Keras library optimiser) with a learning rate of 1e-5<br/>

#PRESENTATION - <br/>
Link to the DRIVE presentation = <br/>
https://docs.google.com/presentation/d/1KS2bBm28SLbgyq2vkL1HIRYreWOPGYJicBzfyRfgEIY/edit?ts=5ecbb144#slide=id.g85c9cc7a25_0_0 <br/>
(Open with BITS Mail only)<br/>



