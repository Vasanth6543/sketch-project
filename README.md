🔖 Project Title
Image to Pencil Sketch Conversion Using Python and OpenCV

📝 Abstract
This project aims to convert a given image into a pencil sketch using Python and OpenCV. The process involves image preprocessing techniques such as grayscale conversion, inversion, Gaussian blurring, and blending to simulate the look of a hand-drawn sketch. The application demonstrates the power of computer vision and image processing in transforming multimedia content creatively.

📌 Objective
To implement a Python script that converts an image into a pencil sketch.

To learn and apply basic OpenCV functions like grayscale, inversion, blurring, and blending.

To understand how digital image transformation works using computer vision techniques.

🛠️ Tools and Technologies Used
Programming Language: Python

Libraries: OpenCV (cv2)

Platform: Windows (compatible with any OS)

IDE: Any code editor (VS Code, PyCharm, etc.)

📁 Project Structure
pgsql
Copy
Edit
sketch-project/
├── sketch.py             ← Python script
├── vasanth.jpg           ← Input image
├── sketch_output.jpg     ← Output (generated after running script)
└── README.md             ← Project description and usage guide
🔧 Requirements
Python 3.x

OpenCV Library

🔹 Installation
Use pip to install OpenCV:

bash
Copy
Edit
pip install opencv-python
📷 Methodology (How It Works)
Read the Image
The image is loaded from disk using cv2.imread().

Convert to Grayscale
The image is converted to a grayscale image to simplify the transformation.

Invert the Image
Each pixel value is inverted (255 - pixel) to enhance sketch effect.

Apply Gaussian Blur
A Gaussian Blur is applied to soften the image and mimic shading.

Blend Using Color Dodge
The grayscale image is divided by the inverted-blurred image using cv2.divide() to highlight the edges and details, giving a pencil sketch appearance.

Display and Save
The original and sketch images are displayed, and the sketch is saved as sketch_output.jpg.

💻 Code Overview
python
Copy
Edit
import cv2

# Load image
image = cv2.imread("vasanth.jpg")
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
inverted = 255 - gray
blurred = cv2.GaussianBlur(inverted, (21, 21), 0)
inverted_blurred = 255 - blurred
pencil_sketch = cv2.divide(gray, inverted_blurred, scale=256.0)

cv2.imshow("Original", image)
cv2.imshow("Sketch", pencil_sketch)
cv2.imwrite("sketch_output.jpg", pencil_sketch)
cv2.waitKey(0)
cv2.destroyAllWindows()
✅ Features
Simple and fast image processing

Lightweight and easy to use

Supports any .jpg or .png image

Real-time preview of sketch output

📈 Results
The script successfully converts any input image into a pencil sketch.

The output is saved automatically and can be used for creative purposes such as profile images, posters, or fun projects.

🧪 Sample Output
Input Image: vasanth.jpg

Output Image: sketch_output.jpg (generated)

🧠 Learning Outcomes
Understanding image transformation techniques using OpenCV

Working with Python libraries for real-time image processing

Hands-on practice with grayscale conversion, image inversion, and blending

Experience with GitHub for version control and project sharing

🔐 License
This project is licensed under the MIT License, allowing reuse with attribution.

🙋‍♂️ Future Enhancements
Add GUI using Tkinter or PyQt

Allow drag-and-drop image uploads

Export output in different artistic styles (e.g., color sketch, cartoon, etc.)

Build a web-based app using Flask or Streamlit

📬 Author
Name: Vasanth S

GitHub: @Vasanth6543
