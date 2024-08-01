Image Processing with Non-AI Methods
Overview
This script performs image processing to detect and count objects (screws) using non-AI techniques. It processes images by applying various image processing techniques to generate masks and extract detected objects.

How It Works
Directory Paths:

image_directory: Path to the directory containing the input images.
output_directory: Path to the directory where the processed images and masks will be saved.
Function: process_image(image_path)

Load Image: Reads the image from the specified path.
Convert to Grayscale: Converts the image to a grayscale format to simplify processing.
Blurring: Applies Gaussian blur to reduce noise and smooth the image.
Adaptive Thresholding: Applies adaptive thresholding to create a binary image where objects are highlighted against a background.
Morphological Operations: Uses morphological operations (closing and opening) to clean up the binary image and remove small noise.
Contour Detection: Finds contours in the binary image that represent potential objects.
Contour Filtering: Filters contours based on their area to discard irrelevant ones and keep only significant objects.
Mask Creation: Creates a mask image where detected objects are highlighted.
Output Image Generation: Applies the mask to the original image to highlight detected objects.
Count Objects: Counts the number of filtered contours.
Processing and Saving Images:

Iterates through each image in the image_directory.
Calls process_image(image_path) for each image to get the processed output and mask.
Saves the processed images and masks to the output_directory with appropriate filenames (output_<filename> for the processed image and mask_<filename> for the mask).
Output:

Processed Images: Images with detected objects highlighted.
Masks: Binary masks where detected objects are marked.
Requirements
OpenCV: The script uses OpenCV for image processing tasks. Ensure you have OpenCV installed in your Python environment.
