🛢️ SpillGuard: Oil Spill Detection with U-Net :

     This project implements an oil spill segmentation system using a U-Net deep learning model. The system is trained on satellite images and masks to detect oil
     spills, and provides a Flask-based web interface for real-time predictions.


📌 Features :

   --> Automated dataset extraction and preprocessing (images + masks).

   --> U-Net based segmentation for oil spill detection.

   --> Model training with checkpointing and extended training capability.

   --> Visual comparison of original image, ground truth mask, and predicted mask.

   --> Flask web app with upload interface for real-time oil spill detection.

   --> Overlay visualization (original image + predicted mask heatmap).


⚙️ Installation :

    1.Clone the repository.

    2.Install the required dependencies (TensorFlow, Keras, Flask, OpenCV, Matplotlib, etc.).

    3.If using Google Colab, mount Google Drive to load dataset and save models.



📊 Dataset :

   --> The dataset should include images and masks, organized into train, val, and test splits.

   --> Images are resized to 128x128 and normalized to values between 0 and 1.

   --> Masks are grayscale and used for binary segmentation (oil spill vs. background).



🏗️ Model: U-Net Architecture : 

     Encoder: Convolution + MaxPooling layers for hierarchical feature extraction.

     Bottleneck: Deep feature representation capturing spatial patterns.

     Decoder: Transposed convolutions with skip connections for reconstruction.

     Output: Binary segmentation mask (sigmoid activation).

Loss function: Binary Crossentropy
Optimizer: Adam (learning rate = 1e-4)
Evaluation metric: Accuracy



🚀 Training :

     The model is trained on the train set and validated on the val set.

     Checkpointing ensures the best model is always saved.
     
     Training can be resumed from the last saved model for additional epochs.



🧪 Evaluation :

      The trained model is tested on unseen test set images.

      Results are visualized as side-by-side plots:

      Original image

      Ground truth mask

      Predicted mask

   This helps assess segmentation quality.



🌐 Flask Web App :

     Provides a simple upload interface.

     Users can upload satellite images.
 
    The app returns:

    Original image

    Predicted segmentation mask

   Heatmap overlay of oil spill regions


DEPLOYED LINK : https://huggingface.co/spaces/Dillu2004/spillguard-oil-detection
