# Plant Leaf Disease Image Classification

Ini merupakan project dari submission akhir pada **Belajar Pengembangan Machine Learning** di Dicoding. Tujuan dari proyek ini adalah untuk mengklasifikasikan penyakit pada daun tanaman menggunakan **teknik klasifikasi citra berbasis deep learning**.

## 📌 Tujuan Proyek

Proyek ini bertujuan untuk:
- Mengembangkan model deep learning untuk **mengklasifikasikan berbagai jenis penyakit pada daun tanaman**.
- Meningkatkan deteksi dini penyakit tanaman guna mencegah penyebaran dan memungkinkan pengobatan yang lebih cepat.
- Memanfaatkan dataset citra daun tanaman untuk melatih dan mengevaluasi model.

## 📑 Metodologi

### 1️⃣ Data Collection
- Menggunakan dataset yang terdiri dari gambar daun tanaman sehat dan yang terinfeksi penyakit.
- Dataset dapat diakses di pranala berikut: [PlantVillage Dataset](https://github.com/spMohanty/PlantVillage-Dataset/tree/master/raw/color).
- Mengecek jumlah kelas/subfolder di dalam dataset, menampilkan nama setiap kelas, menghitung jumlah gambar dalam setiap kelas, serta mendapatkan resolusi unik setiap gambar.

### 2️⃣ Preprocessing Data
- Memfokuskan pada kelas **"Tomato"** dalam dataset.
- Mengidentifikasi subkelas dari "Tomato".
- Menghitung jumlah gambar dalam setiap subkelas, serta mencatat resolusi unik dari setiap gambar karena memiliki ukuran yang berbeda-beda.

### 3️⃣ Dataset Splitting
- Dataset dibagi menjadi **80% Train Set dan 20% Test Set**.

### 4️⃣ Dataset Augmentation
- Menggunakan **ImageDataGenerator** untuk melakukan augmentasi pada Train Set.
- Train Set mengalami augmentasi seperti rotasi, flipping, dan zooming agar model lebih general.
- Test Set hanya dilakukan **rescaling** untuk mempertahankan integritas data uji.

### 5️⃣ Pengembangan Model
- Membangun arsitektur **Convolutional Neural Network (CNN)** sebagai model utama.
- Menggunakan model **pretrained** (MobileNetV2) untuk **transfer learning** agar meningkatkan akurasi model.
- Mengimplementasikan callback seperti **Early Stopping** untuk mencegah overfitting.
- Melatih model menggunakan **optimizer Adam** dan **loss function categorical_crossentropy** yang sesuai untuk klasifikasi multi-kelas.

### 6️⃣ Evaluasi Model
- Mengevaluasi performa model pada training dan testing set.
- Menampilkan akurasi serta loss untuk masing-masing dataset.

    **Hasil Evaluasi Model:**
    - **Training Accuracy:** 99.70%
    - **Training Loss:** 0.3754
    - **Testing Accuracy:** 96.21%
    - **Testing Loss:** 0.5071

![Grafik Performa Model](https://github.com/user-attachments/assets/95fbf9e7-fc66-45c9-b852-e8830217e1a0)


### 7️⃣ Model Convertion
- Menyimpan model yang telah dilatih dalam berbagai format:
  - `.h5` dan `.keras`.
  - **SavedModel** untuk TensorFlow.
  - **TF-Lite** untuk deployment di perangkat mobile.
  - **TensorFlow.js** untuk penggunaan berbasis web.

### 8️⃣ Inference
- Melakukan prediksi menggunakan model TF-Lite.
- Menggunakan gambar yang diambil dari internet untuk menguji prediksi. [Link](https://th.bing.com/th/id/OIP.Js8__bryYlncSSuNOAIyWgAAAA?rs=1&pid=ImgDetMain)

![Prediksi](https://github.com/user-attachments/assets/f039d2f9-9182-42b8-b61d-b33729d2b276)


## 📊 Submission Review
<img width="936" alt="Review" src="https://github.com/user-attachments/assets/f16f5906-4868-4808-9f12-0d316c41521b" />


## 📌 Conclusion
Pada proyek ini, saya melakukan **klasifikasi citra berbasis deep learning** untuk mendeteksi penyakit pada daun tanaman **Tomat**. Model ini dapat dikembangkan lebih lanjut dengan dataset yang lebih besar serta penyempurnaan arsitektur untuk meningkatkan akurasi.

**Author:** Mellisa  
**Date:** 11-11-2024  
**Tools:** Python, TensorFlow, Keras, Matplotlib

