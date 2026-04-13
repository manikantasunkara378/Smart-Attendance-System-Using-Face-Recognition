# 🎓 Smart Attendance System Using Face Recognition

![Python](https://img.shields.io/badge/Python-3.10-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green)
![face--recognition](https://img.shields.io/badge/face--recognition-1.3.0-orange)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-yellow)
![License](https://img.shields.io/badge/License-MIT-red)

An automated student attendance system built using **deep learning-based face recognition**. The system detects and identifies student faces from classroom photographs and records attendance with Indian Standard Time (IST) timestamps — no manual roll call needed.

---

## 📸 Demo

| Upload Student Photos | Upload Class Photo | Attendance Marked |
|---|---|---|
| Individual ID photos | Group / single photo | CSV downloaded |

---

## ✨ Features

- ✅ Detects multiple faces in a single classroom photo
- ✅ Identifies students using 128-dimensional face embeddings
- ✅ Records attendance with accurate IST timestamps
- ✅ Exports attendance to downloadable CSV
- ✅ Supports JPG, PNG, WebP image formats
- ✅ Unknown faces flagged in red — not marked present
- ✅ Runs entirely on Google Colab — no local setup needed

---

## 🛠️ Technologies Used

| Library | Purpose |
|---|---|
| `face_recognition` | Face detection and 128-d encoding |
| `dlib` | Deep learning face landmark model |
| `OpenCV` | Image processing |
| `NumPy` | Array operations |
| `Pillow (PIL)` | Image format handling |
| `pytz` | Indian Standard Time (IST) |
| `Google Colab` | Cloud execution environment |

---

## 🚀 How to Run (Google Colab)

### Step 1 — Open Google Colab
Go to [colab.research.google.com](https://colab.research.google.com) and open the notebook.

### Step 2 — Run Cell 1: Install Libraries
```python
!pip install face-recognition
!pip install opencv-python-headless
!pip install pytz
```

### Step 3 — Run Cell 2: Mount Google Drive
```python
from google.colab import drive
drive.mount('/content/drive')
```

### Step 4 — Run Cell 3: Upload Student Photos
- Upload individual student ID photos
- Name them as `STUDENTID.jpg` (e.g. `VTU28789.jpg`)

### Step 5 — Run Cell 4: Encode Faces
- System automatically encodes all uploaded faces
- Tries multiple scales for reliable detection

### Step 6 — Run Cell 5: Upload Classroom Photo
- Upload a classroom or group photo
- System detects all faces and marks attendance

### Step 7 — Run Cell 6: Download CSV
- Attendance saved as `Attendance.csv`
- Contains Name and Time (IST) columns

---

## 📁 Project Structure

```
Smart-Attendance-System/
│
├── ImagesAttendance/
│   └── VTU28789.jpg        # Student ID photos (one per student)
│
├── main.py                 # Local Windows version
├── SmartAttendance.ipynb   # Google Colab notebook
├── Attendance.csv          # Sample attendance output
├── README.md               # Project documentation
└── .gitignore
```

---

## 📊 Sample Output

**Attendance.csv**
```
Name,       Time (IST)
VTU28789,   11:45:32
VTU28790,   11:45:32
VTU28791,   11:45:33
```

**Console Output**
```
Loading Images...
  ✅ Loaded: VTU28789.jpg
Encoding Complete — 1/1 encoded

Faces detected: 3
  ✅ Marked: VTU28789 at 11:45:32 IST
  ✅ Marked: VTU28790 at 11:45:32 IST
  ✅ Marked: VTU28791 at 11:45:33 IST

Total marked: 3
```

---

## ⚠️ Tips for Best Results

| ✅ Do This | ❌ Avoid This |
|---|---|
| Use clear front-facing photos | Side profile photos |
| Good lighting | Dark or blurry photos |
| `.jpg` format for ID photos | Snapchat / filtered photos |
| One face per ID photo | Group photos as ID photos |

---

## 🔮 Future Improvements

- [ ] Live webcam feed for real-time attendance
- [ ] Web dashboard for teachers
- [ ] Firebase/MySQL database integration
- [ ] Email/SMS alerts for absent students
- [ ] CNN model for improved accuracy

---

## 📚 References

1. Adam Geitgey — [face_recognition library](https://github.com/ageitgey/face_recognition)
2. Davis E. King — Dlib Machine Learning Toolkit, JMLR 2009
3. F. Schroff et al. — FaceNet: A Unified Embedding for Face Recognition, CVPR 2015
4. N. Dalal & B. Triggs — HOG for Human Detection, IEEE CVPR 2005
5. OpenCV — [opencv.org](https://opencv.org)

---

## 👨‍💻 Author

**Manikanta** — VTU28789
Department of Computer Science & Engineering

---

## 📄 License

This project is licensed under the MIT License.