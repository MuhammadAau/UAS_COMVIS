# UAS_COMVIS
Model Deteksi Objek dengan YOLOv8
👥 Nama Kelompok:
Shalaudin Muhammad Sah - G1A022070
Hanif Abdullah Zuhdi - G1A022041

📘 Deskripsi Proyek
  Proyek ini bertujuan untuk membangun sistem deteksi objek berbasis YOLOv8 guna mengidentifikasi keberadaan helm dan rompi keselamatan pada pekerja proyek konstruksi. Sistem ini dirancang untuk meningkatkan kepatuhan terhadap protokol keselamatan kerja menggunakan rekaman dari CCTV atau gambar proyek.
Model dilatih menggunakan dataset anotasi objek yang diperoleh dari Kaggle dalam format YOLO. Proses pengembangan meliputi pelatihan model, evaluasi kinerja, serta visualisasi hasil deteksi pada gambar uji.

🧰 Fitur Utama
✅ Mengimpor dan mempersiapkan dataset anotasi YOLO dari file .zip.
✅ Pelatihan model YOLOv8 dengan menggunakan Google Colab dan GPU.
✅ Evaluasi model berdasarkan metrik deteksi seperti mAP50, precision, dan recall.
✅ Visualisasi hasil deteksi objek (helm dan rompi) pada gambar uji.
✅ Ekspor model dalam format .pt untuk keperluan deployment lanjutan.

🛠️ Teknologi dan Library yang Digunakan
Python 3.x
Ultralytics YOLOv8
Google Colab
OpenCV
Matplotlib
Kaggle API (opsional jika dataset diunduh langsung)

 Struktur Notebook
Notebook ini terdiri dari beberapa bagian utama sebagai berikut:

1. 📦 Import Library
Memuat seluruh dependensi dan pustaka yang diperlukan dalam proyek, termasuk:

os, zipfile – untuk manipulasi file dan direktori

ultralytics – untuk pemodelan YOLOv8

cv2 (OpenCV) – untuk pemrosesan gambar

matplotlib.pyplot – untuk visualisasi hasil

2. ☁️ Upload Data dari Kaggle
Menggunakan token API atau file .zip dari Google Drive/Kaggle untuk mengunduh dan mengekstrak dataset anotasi objek (format YOLO) ke Google Colab.

Jika dataset dalam bentuk .zip, dilakukan proses ekstraksi dan penyesuaian struktur folder agar sesuai dengan format YOLO (images/train, labels/train, dll).

3. 🤖 Modeling dan Pelatihan YOLOv8
Pada bagian ini dilakukan:

Pembuatan file konfigurasi .yaml untuk YOLOv8

Pemanggilan model YOLOv8 (misalnya: yolov8n.pt)

Training model selama sejumlah epoch dengan dataset yang telah disiapkan

Pengaturan ukuran gambar, batch size, dan parameter lainnya

4. 🧪 Uji Coba Model
Setelah proses pelatihan selesai, model diuji pada data validasi atau gambar uji secara manual. Output berupa nilai evaluasi model seperti:

mAP50 (mean Average Precision)

Precision

Recall

5. 🖼️ Visualisasi Hasil
Menampilkan hasil deteksi objek dari model pada gambar uji. Hasil ditunjukkan dalam bentuk bounding box dengan label seperti helmet atau vest.

Visualisasi dilakukan menggunakan:

model.predict(...) dari Ultralytics

cv2 atau matplotlib untuk menampilkan gambar

HASIL AKHIR
Model berhasil mengenali objek helm dan rompi pada gambar uji.
Deteksi akurat tergantung kualitas dan jumlah data pelatihan.
Model dapat di-export dan digunakan untuk deployment lebih lanjut.
