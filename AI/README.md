YOLOv5 Object Detection for Screws
Overview
This script uses the YOLOv5 object detection model to process images and detect screws. It reads images, applies the YOLOv5 model for detection, and visualizes the results with bounding boxes and labels. The script also counts the number of detected objects in each image.

How It Works
Model Loading:

YOLOv5 Model: The script loads the pre-trained YOLOv5s model from the ultralytics library. YOLOv5 is a state-of-the-art object detection model known for its speed and accuracy.
Function: detect_and_count(image_path)

Load Image: Reads the image from the specified path in BGR format (default for OpenCV).
Convert to RGB: Converts the image from BGR to RGB format, which is required for the YOLOv5 model.
Perform Inference: Runs the YOLOv5 model to detect objects in the image. The results include bounding boxes, confidence scores, and class labels.
Count Detected Items: Counts the number of bounding boxes (detected items).
Draw Bounding Boxes: Draws bounding boxes and labels on the image to visualize the detected objects.
Display Results: Uses Matplotlib to display the image with bounding boxes. The image is converted back to RGB format for display purposes.
Processing Images:

Directory Path: Specifies the directory containing the images to be processed.
Image Iteration: Iterates through each image file in the directory with extensions .jpg or .png.
Detection and Counting: Calls detect_and_count(image_path) for each image, prints the filename and the count of detected items.
Requirements
PyTorch: Required for running the YOLOv5 model. Ensure you have the PyTorch library installed.
OpenCV: Required for image processing tasks. Ensure you have OpenCV installed.
Matplotlib: Used for displaying images with bounding boxes. Ensure you have Matplotlib installed.
Google Colab (Optional): If running in Google Colab, use cv2_imshow instead of cv2.imshow for displaying images.
