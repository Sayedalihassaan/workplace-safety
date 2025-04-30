
---

## 🦺 Safety Helmet and Vest Detection

This project uses a custom YOLOv5 model to detect **helmets**, **safety vests**, and **workers** in video footage. It processes each frame of a video, identifies whether individuals are wearing the required safety gear, and highlights those who aren't — saving their images for review.

---

### 📸 Example Use Case

- **Input**: Surveillance footage from a construction site
- **Output**: Annotated video (`output.mp4`) + individual images of non-compliant workers (`output/` folder)

---

### 🚀 Features

- Detects three object classes: `Helmet`, `Vest`, and `Worker`
- Identifies and saves snapshots of workers missing safety gear
- Processes video frame-by-frame using OpenCV
- Uses a fine-tuned YOLOv5 model

---

### 🛠 Requirements

- Python 3.8+
- PyTorch
- OpenCV
- YOLOv5 (via `torch.hub`)

Install dependencies with:

```bash
pip install torch opencv-python numpy
```

---

### 📂 File Structure

```
📁 yolov5safetyhelmet/
│   ├── best final.pt          # Custom trained YOLOv5 model
│   ├── video2.ts              # Input video
│   ├── vest and helmet.ipynb  # This notebook
│   ├── output.mp4             # Output video
│   └── output/                # Detected violations (images)
```

---

### ▶️ How to Run

1. Place your model (`best final.pt`) and input video (`video2.ts`) in the same folder.
2. Open the Jupyter notebook `vest and helmet.ipynb`.
3. Run all cells. This will:
   - Load the YOLOv5 model
   - Process the video frame-by-frame
   - Save the output video and violation images

---

### 📦 Output

- ✅ Annotated video with bounding boxes
- ❌ Individual images of workers not wearing helmets/vests
- ✅ Real-time display window while processing

---

### 📝 License

This project is for educational and safety compliance research purposes. You may customize it under your own license.

---

