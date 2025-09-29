## Dataset

Dataset yang digunakan pada tugas ini ini berasal dari [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia) yang tersedia di Kaggle.  
Namun, dalam penelitian ini hanya digunakan 5 Gambar
<img width="2583" height="647" alt="image" src="https://github.com/user-attachments/assets/76c52472-76e2-49ff-9c4b-7e9655ae5456" />

## Image Enhancement
## a. Grayscale
Citra warna dikonversi menjadi grayscale. Proses ini mengurangi kompleksitas data karena hanya menyimpan informasi intensitas cahaya, tanpa warna.
## b. Gausian Blur
Gaussian blur digunakan untuk mengurangi noise halus pada citra dengan cara melakukan konvolusi menggunakan kernel berbasis distribusi Gaussian. Efeknya membuat citra sedikit lebih halus sehingga detail acak (noise) tidak mendominasi sebelum tahap peningkatan kontras.
## c. CLAHE
CLAHE meningkatkan kontras citra dengan membagi gambar menjadi blok kecil, lalu melakukan histogram equalization pada tiap blok. Dengan clip limit (2.0), peningkatan kontras tetap terkontrol sehingga noise tidak ikut diperkuat.
## d. Resized
Citra hasil CLAHE diubah ukurannya menjadi (128 × 128) dengan mempertahankan rasio aspek (aspect ratio). Jika rasio tidak sama, area kosong diisi dengan padding (warna hitam) agar setiap citra berukuran sama
