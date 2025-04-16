# Vehicle-ReId
This project focuses on vehicle re-identification (Vehicle ReID) using deep learning techniques. The goal is to recognize the same vehicle across images captured by different cameras in urban surveillance scenarios. The project is based on the [VeRi-776](https://github.com/VehicleReId/VeRi) dataset, a widely-used benchmark in the research community for vehicle re-identification.

## Repository Contents
  * **Color_Type_VeRi_ReiD.ipynb**: Exploratory data analysis (EDA) of the VeRi-776 dataset, focusing on vehicle attributes like color and type.
  * **Vehicle_ReId_CNN_ContrastiveLoss.ipynb**: A CNN-based model for vehicle re-identification using contrastive loss.
  * **Vehicle_ReId_CNN_TripletLoss.ipynb**: A CNN-based model for vehicle re-identification using triplet loss.

## Dataset
This project uses the [VeRi-776](https://github.com/VehicleReId/VeRi) dataset, which contains over 50,000 images of 776 vehicles captured by 20 cameras within a 1 km² urban area over a 24-hour period. It provides detailed annotations including:
  * Vehicle ID: Unique identifier for each vehicle.
  * Camera ID: ID of the camera that captured the image.
  * Attributes: Color, type, and brand of the vehicle.
  * Spatio-temporal information: Timestamps and camera positions.

To download the dataset, users must send an email request to the authors providing their full name and affiliation. The dataset is intended for non-commercial research use only.

## Expected Results
The trained models should be able to correctly re-identify the same vehicle across different camera views, despite changes in angle, lighting, and occlusions. Common evaluation metrics include:
  * **Rank-K Accuracy**: How often the top-K match is correct.
  * **Mean Average Precision (mAP)**: The mean of average precisions across all queries.

| Notebook Name                        | Rank-1 Accuracy | Rank-5 Accuracy | Rank-5 Accuracy | mAP    |
|--------------------------------------|-----------------|-----------------|-----------------|--------|
| Vehicle_ReId_CNN_ContrastiveLoss     | 26.16%          | 56.54%          | 70.27%          | 14.96% |
| Vehicle_ReId_CNN_TripletLoss         | 73.69%          | 90.93%          | 94.92%          | 25.09% |
