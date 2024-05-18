# Remove-EG-logo
Given a picture of an Egyptian national id, you are tasked to remove the logo of "جمهورية مصر العربية" and replace it with the color of its background, see attached examples.

# Solution:
## Prepare and Annotate Data:
    Obtain the dataset from Kaggle and annotate it using Roboflow.
    Export the annotated data in YOLOv5 format.
    - [Kaggle Link](https://www.kaggle.com/datasets/mostafaebrahiem/egyptian-ids)
    - [Annotated Data](https://app.roboflow.com/cairo-university-vqdin/fine_tuned/1)

## Object Detection with YOLOv5:
    Use YOLOv5 to detect the text "جمهورية مصر العربية" in the image.
    Save the coordinates of the detected bounding box to a text file.

## Load the Image and Coordinates:
    Read the image using OpenCV.
    Parse the coordinates from the text file to get the region of interest (ROI) where the text is located.

## Extract the ROI:
    Extract the region of interest (ROI) from the image using the coordinates obtained from YOLOv5.

## Cluster the Colors in the ROI:
    Apply k-means clustering to the colors within the ROI to identify the most common colors.
    Choose a reasonable number of clusters (e.g., 5 clusters).

## Select the Background Color:
    Determine the lightest color among the clusters, as this is most likely the background color.

## Replace the Text with the Background Color:
    Fill the bounding box of the detected text with the selected background color.
## Dataset
    - [Kaggle Link](https://www.kaggle.com/datasets/mostafaebrahiem/egyptian-ids)
    - [Annotated Data](https://app.roboflow.com/cairo-university-vqdin/fine_tuned/1)
