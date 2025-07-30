Image to Pencil Sketch Conversion Using Python and OpenCV

🔖 1. Project Title
Image to Pencil Sketch Conversion Using Python and OpenCV

📝 2. Abstract
This project focuses on converting a digital image into a pencil sketch using Python and the OpenCV library. It demonstrates basic image processing techniques such as grayscale transformation, inversion, blurring, and image blending to simulate the appearance of a hand-drawn pencil sketch. The project highlights how computer vision can be creatively used in multimedia and artistic applications.

📌 3. Objectives
To develop a Python script that converts a color image into a pencil sketch.

To understand and implement basic OpenCV operations such as:

Grayscale conversion

Image inversion

Gaussian blur

Image blending

To explore real-time digital image processing using computer vision.

🛠️ 4. Tools and Technologies Used
Programming Language: Python

Libraries: OpenCV (cv2)

Operating System: Windows (Compatible with Linux/macOS)

IDE/Editor: Visual Studio Code / PyCharm / Any text editor

📁 5. Project Directory Structure
pgsql
Copy
Edit
sketch-project/
├── sketch.py             ← Main Python script
├── vasanth.jpg           ← Input image (can be replaced with any image)
├── sketch_output.jpg     ← Output pencil sketch (auto-generated)
└── README.md             ← Documentation file

🔧 6. Requirements
Python 3.x

OpenCV (cv2) Python library

🔹 Installation:
To install OpenCV, run:

bash
Copy
Edit
pip install opencv-python
📷 7. Methodology (Working Process)
The project follows these image transformation steps:

Reading the Image
Load the image using cv2.imread().

Grayscale Conversion
Convert the color image to a grayscale image for simplicity.

Inversion
Invert the grayscale image using 255 - pixel_value.

Gaussian Blur
Apply a blur using cv2.GaussianBlur() to create a soft shading effect.

Blending (Color Dodge)
Use cv2.divide() to blend the grayscale and blurred image. This operation highlights edges and creates the pencil sketch effect.

Display and Save
Display the original and sketch images using cv2.imshow() and save the output using cv2.imwrite().

💻 8. Code Overview
python
Copy
Edit
import cv2

# Load image
image = cv2.imread("vasanth.jpg")

# Convert to grayscale
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Invert the grayscale image
inverted = 255 - gray

# Apply Gaussian blur
blurred = cv2.GaussianBlur(inverted, (21, 21), 0)

# Invert the blurred image
inverted_blurred = 255 - blurred

# Blend using color dodge
pencil_sketch = cv2.divide(gray, inverted_blurred, scale=256.0)

# Show images
cv2.imshow("Original", image)
cv2.imshow("Sketch", pencil_sketch)

# Save result
cv2.imwrite("sketch_output.jpg", pencil_sketch)

# Close display windows
cv2.waitKey(0)
cv2.destroyAllWindows()
✅ 9. Features
Converts any .jpg or .png image to a pencil sketch

Lightweight and simple implementation

Real-time preview of the sketch

Automatic saving of the output image

Easy to modify and extend

📈 10. Results
The Python script successfully generates a pencil sketch version of the input image.

The resulting sketch is saved as sketch_output.jpg in the project folder.

It mimics the look of a hand-drawn sketch, suitable for creative usage.

🧠 11. Learning Outcomes
Hands-on understanding of computer vision basics using OpenCV.

Learned techniques like grayscale conversion, image inversion, Gaussian blur, and color dodge blending.

Understood how to work with Python libraries for image manipulation.

Gained experience in GitHub project setup and version control.

🔐 12. License
This project is open-source and licensed under the MIT License.
You are free to use, modify, and distribute the code with attribution.

🙋‍♂️ 13. Future Enhancements
Add a graphical user interface (GUI) using Tkinter or PyQt

Allow drag-and-drop for input images

Export sketches in different styles (color pencil, cartoon, charcoal, etc.)

Convert into a web application using Flask or Streamlit

Add batch processing for multiple images at once

📬 14. Author
Name: Vasanth S

GitHub: @Vasanth6543
