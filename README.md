
# Animal Image Classification using CNN and MobileNetV2

Proyek ini merupakan implementasi klasifikasi gambar hewan menggunakan Deep Learning dengan arsitektur Convolutional Neural Network (CNN) berbasis transfer learning MobileNetV2 menggunakan TensorFlow dan Keras.

## Dataset
Dataset yang digunakan adalah Animals-10 Dataset dari Kaggle:
- Sumber dataset: [Animals-10 Dataset](https://www.kaggle.com/datasets/alessiocorrado99/animals10)
- Jumlah kelas: 10 kelas hewan
- Total gambar: > 26.000 gambar

### Kelas Dataset
- cane : Anjing
- cavallo : Kuda
- elefante : Gajah
- farfalla : Kupu-kupu
- gallina : Ayam
- gatto : Kucing
- mucca : Sapi
- pecora : Domba
- ragno : Laba-laba
- scoiattolo : Tupai


## Library yang Digunakan
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-Learn
- Pillow
- Split-Folders
- TensorFlowJS


## Tahapan Proyek
### 1. Data Preparation
- Download dataset dari Kaggle
- Visualisasi distribusi dataset
- Visualisasi sampel gambar tiap kelas
- Split dataset:
  - Train Set
  - Validation Set
  - Test Set

### 2. Data Preprocessing
Menggunakan preprocessing dari MobileNetV2:
- Resize image
- Normalisasi menggunakan `preprocess_input`
- Data augmentation:
  - Horizontal Flip
  - Rotation
  - Zoom
  - Width Shift
  - Height Shift

### 3. Model Architecture
Model dibangun menggunakan:
- Sequential API
- MobileNetV2 sebagai feature extractor
- Conv2D Layer
- MaxPooling Layer
- BatchNormalization
- Dropout
- Dense Layer

### 4. Callback Implementation
Model menggunakan callback:
- EarlyStopping
- ReduceLROnPlateau
- ModelCheckpoint

### 5. Training dan Evaluasi
Model dilatih menggunakan GPU pada Google Colab.

Hasil evaluasi model:
- Test Accuracy : 96.31%
- Test Loss : 0.6113

### 6. Visualisasi
Proyek ini menampilkan:
- Plot Accuracy
- Plot Loss
- Confusion Matrix

### 7. Inference
Model dapat melakukan prediksi gambar hewan menggunakan SavedModel TensorFlow.

Inference dilakukan dengan:
- Load SavedModel
- Input gambar baru
- Prediksi kelas hewan
- Menampilkan confidence score

### 8. Export Model
Model berhasil diexport ke beberapa format:
- SavedModel
- TensorFlow Lite (TFLite)
- TensorFlow.js (TFJS)
