# 👀 Face Detection using OpenCV

![OpenCV Banner](https://opencv.org/wp-content/uploads/2020/07/OpenCV_logo_white_600x.png)

A simple yet powerful project demonstrating real-time **face detection** using OpenCV and Haar Cascade classifiers. This project processes images to identify and mark human faces, showcasing the capabilities of classical computer vision techniques without deep learning.

---

## 🧠 What’s Inside

- ✅ Face detection using OpenCV's Haar Cascade
- ✅ Image pre-processing (grayscale conversion)
- ✅ Bounding box visualization on detected faces
- ✅ Minimal and clean UI using Jupyter Notebook
- ✅ Tested on cartoon images (Simpsons dataset) for fun

---

## 📸 Example Output

### Original Image

![Original](sample_images/output_1.png)

### Detected Face(s)

![Detected](sample_images/output_2.png)

---

## 🚀 How It Works

1. Load an image using OpenCV.
2. Convert the image to grayscale for better accuracy.
3. Load Haar cascade classifier from OpenCV’s pre-trained models.
4. Detect faces using `detectMultiScale()`.
5. Draw rectangles around detected faces.

---

## 🛠️ Requirements

Install dependencies with:

```bash
pip install opencv-python
```

> *Jupyter Notebook support recommended for interactive exploration.*

---

## 📁 File Structure

```
├── opencvsimpsons.ipynb       # Main notebook with face detection logic
├── README.md                  # This file
```

---

## 🧪 Sample Code Snippet

```python
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + "haarcascade_frontalface_default.xml")
img = cv2.imread("homer.jpg")
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
faces = face_cascade.detectMultiScale(gray, 1.1, 4)

for (x, y, w, h) in faces:
    cv2.rectangle(img, (x, y), (x+w, y+h), (255, 0, 0), 2)
cv2.imshow("Detected Face", img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

---

## 🎯 Future Improvements

- Add webcam support for live face detection
- Improve accuracy with DNN or CNN-based models
- Integrate a GUI using Tkinter or PyQt
- Face recognition using LBPH or FaceNet

---

## 🙌 Acknowledgements

- [OpenCV Documentation](https://docs.opencv.org/)
- Haar Cascades by [Viola-Jones Algorithm](https://en.wikipedia.org/wiki/Viola%E2%80%93Jones_object_detection_framework)

---

## 📬 Contact

**Arpan Jain**  
📧 https://arpanjainportfolio.netlify.app/  
🌐 [LinkedIn](https://www.linkedin.com/in/arpan-jain-3b8075258/)
