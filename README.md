<p align="center">
  <img width=75% src="https://github.com/themichaelmort/cancer_detection/blob/main/cancer_detector.gif" alt="Time-lapse learning to detect cancer">
  
</p>
<p align="center">
  This time lapse shows the deep neural net learning to detect the cancerous cells in a tissue sample slide. (You may have to wait a moment for the animation to show the learning. Look for grey splotches that change size.)
</p>
 
<h1>Cancer Detection</h1>

<p>
  The human body is a mind-breakingly complicated system, and when something goes wrong it is a notoriously difficult system to debug. Deep learning models such as the convolutional neural network (CNN) are powerful tools for extracting detailed patterns from complex images. In this project, I trained a small CNN on slide images of cells to identify the portions of those images that contained cancerous cells.
</p>

<h2>At a Glance</h2>

<ul>
  <li>Dataset - Cancer Dataset, can be downloaded from http://liftothers.org/cancer_data.tar.gz</li>
  <li>Models - U-net. The U-net is a convolutional neural network with extra connections. The U-net I implemented for this project is adapted from the work of <a href="https://arxiv.org/pdf/1505.04597.pdf">Ronneberger et al.</a></li>
  <li>Optimizer - Adam, as implemented in PyTorch</li>
  <li>Loss function - Cross Entropy Loss, as implemented in PyTorch</li>
    <ul>
      <li>Note: The script Unet_cancer_detection.py was drafted in Google colab. It assumes acces to a cuda enabled GPU for training.</li>
    </ul>
</ul>

<h2>Remarks</h2>
<p>
  Note how the cancer detector in the animation above seems to pulse about the cancerous area of the picture. This is likely because the dataset used for training was hand-labled. As a result, the boundary between cancerous and non-cancerous is somewhat arbitrary. (The annotation was just meant to encircle cancerous cells or groups of cells, not merely flag the cancerous cells parts. I believe the pulsing behavior is the algorithm trying to match the arbitrary labeling of the dataset. A more precisely labeled dataset might lead to better results. Or, it may be sufficient to have the model alert the user that it thinks a certain percentage of the pixels in an image are cancerous. A high enough percentage would be grounds for further testing.
  </p>
