```markdown
# Object Detection dengan Haar Cascade & Faster R-CNN

Proyek ini menunjukkan dua pendekatan populer dalam object detection:
- **Haar Cascade** menggunakan OpenCV untuk deteksi real-time (misal: deteksi wajah, mata, dan senyum).
- **Faster R-CNN** menggunakan PyTorch (dengan pretrained model dari torchvision) untuk deteksi objek yang lebih kompleks dan akurat.

Data yang digunakan adalah [Aquarium Dataset](https://www.kaggle.com/datasets/sharansmenon/aquarium-dataset?resource=download) dari Kaggle, yang berisi gambar-gambar akuarium dengan anotasi dalam format COCO.

---

## Fitur Utama

- **Deteksi Real-time dengan Haar Cascade:**
  - Implementasi sederhana dan cepat dengan OpenCV.
  - Cocok untuk aplikasi dengan sumber daya terbatas.

- **Deteksi Objek dengan Faster R-CNN:**
  - Fine-tuning model Faster R-CNN (MobileNet V3 Large FPN) untuk mendeteksi kategori objek di dataset akuarium.
  - Evaluasi menggunakan metrik standar seperti mAP@0.5 dan mAP@[0.5:0.95].
  - Visualisasi hasil deteksi yang menarik dengan bounding box dan label yang jelas, menggunakan post-processing Non-Maximum Suppression (NMS).

---

## Hasil Deteksi

Berikut adalah beberapa contoh hasil deteksi menggunakan Faster R-CNN:

![Sample Detection 1](images/sample1.png)
*Figure 1: Hasil deteksi pada gambar sample.*

![Sample Detection 2](images/sample2.png)
*Figure 2: Hasil deteksi pada gambar sample.*

![Sample Detection 3](images/sample3.png)
*Figure 3: Hasil deteksi pada gambar sample.*

*(Anda dapat menambahkan lebih banyak gambar sample di sini)*

---

## Cara Penggunaan

1. **Download Data:**
   - Download dataset dari [Kaggle Aquarium Dataset](https://www.kaggle.com/datasets/sharansmenon/aquarium-dataset?resource=download) dan ekstrak ke direktori kerja Anda.

2. **Instalasi:**
   Pastikan Anda telah menginstal paket-paket berikut:
   ```bash
   pip install opencv-python torch torchvision pycocotools albumentations torchmetrics tqdm
   ```

3. **Menjalankan Proyek:**
   - Untuk **deteksi real-time** menggunakan Haar Cascade, jalankan skrip `haar_cascade_detection.py`.
   - Untuk **training dan inference Faster R-CNN**, jalankan skrip `faster_rcnn_training.py` dan `inference.py` (atau buka notebook `object_detection.ipynb`).

4. **Visualisasi Hasil Inference:**
   - Inference pada data test akan menampilkan gambar dengan bounding box dan label. Label ditampilkan dengan ukuran font besar dan latar belakang hitam agar lebih jelas.

---

## Tentang Proyek

### Haar Cascade
Metode klasik yang memanfaatkan fitur Haar untuk mendeteksi objek. Cocok untuk deteksi sederhana dan real-time, namun memiliki keterbatasan pada variasi objek yang kompleks.

### Faster R-CNN
Pendekatan berbasis deep learning yang menggabungkan Region Proposal Network (RPN) dengan CNN untuk mendeteksi objek. Model ini telah dilatih dengan dataset COCO dan di-fine-tune pada Aquarium Dataset untuk mendeteksi berbagai jenis makhluk laut seperti fish, jellyfish, penguin, puffin, shark, starfish, dan stingray.

---

## Referensi

- [OpenCV Haar Cascades Documentation](https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html)
- [Faster R-CNN Paper](https://arxiv.org/abs/1506.01497)
- [PyTorch Object Detection Tutorial](https://pytorch.org/tutorials/intermediate/torchvision_tutorial.html)
- [Albumentations Documentation](https://albumentations.ai/docs/)
- [TorchMetrics Documentation](https://torchmetrics.readthedocs.io/)

---

## Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE).

---

*Selamat mencoba dan semoga proyek ini bermanfaat untuk Anda!*
```

---

Penjelasan di atas mencakup:
- Deskripsi singkat dan fitur utama dari proyek.
- Hasil deteksi sample (Anda dapat mengganti placeholder gambar dengan link atau path gambar sample yang sebenarnya).
- Instruksi instalasi dan cara menjalankan proyek.
- Referensi dan informasi lisensi.

Anda dapat menyesuaikan bagian-bagian di atas sesuai kebutuhan proyek dan gaya presentasi yang Anda inginkan.
