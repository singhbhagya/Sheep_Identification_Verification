
---

## 🚀 Overview of the Process

### 🔹 Sheep Verification
1. **Input Test Image** → YOLOv8 extracts **face region**.  
2. **Face Model** generates embeddings for the extracted face.  
3. Cosine similarity is computed between test embeddings and stored embeddings of the claimed sheep.  
4. If similarity ≥ threshold → **Verified**, else → **Not Verified**.  

---

### 🔹 Sheep Identification
1. **Input Test Image** → YOLOv8 extracts **face** and **muzzle**.  
2. Face and muzzle embeddings are classified separately using **SVM classifiers**.  
3. The final label is chosen based on the higher confidence score (face vs muzzle).  
4. If confidence ≥ threshold → **Sheep ID predicted**, else → **Unknown**.  

---

## 📑 Documentation
- The **complete methodology, experiments, and results** are available in the PDF reports:
  - [`identification/Sheep IDENTIFICATION.pdf`](identification/Sheep%20IDENTIFICATION.pdf)  
  - [`Verification/sheep_verification.pdf`](Verification/sheep_verification.pdf)

---

## 📊 Datasets and Models
- The datasets used and links to trained models are provided in [`Dataset.txt`](Dataset.txt).  
- Includes both **face and muzzle datasets** and pre-trained YOLOv8 weights.  

---

## ⚙️ Notebooks
- [`YOLOv8_training.ipynb`](YOLOv8_training.ipynb) – Training pipeline for YOLOv8 (face/muzzle detection).  
- [`identification/identification.ipynb`](identification/identification.ipynb) – Sheep identification pipeline.  
- [`Verification/verification_1.ipynb`](Verification/verification_1.ipynb) – Sheep verification pipeline.  

---

## 📌 Results
- Detailed accuracy, precision, recall, confusion matrices, and misclassification analysis are included in the PDFs.  
- Example: [`identification/misclassifications (1).csv`](identification/misclassifications%20(1).csv) contains misclassified instances.  

---

## 🔮 Future Work
- Fuse face + muzzle embeddings for stronger joint representation.  
- Test scalability on larger sheep populations.  

---

## ✨ Acknowledgements
This project was carried out as part of academic research on biometric verification in animals, leveraging modern computer vision techniques.

