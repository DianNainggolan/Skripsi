# Klasifikasi Tingkatan Stres Kerja Berbasis EEG dengan CNN-LSTM  

## 📌 Deskripsi  
Repositori ini berisi kode dan dataset untuk penelitian tentang klasifikasi tingkatan stres kerja menggunakan Electroencephalogram (EEG) dan model deep learning berbasis Convolutional Neural Network - Long Short-Term Memory (CNN-LSTM). Penelitian ini bertujuan untuk mendeteksi serta mengklasifikasikan tingkat stres kerja berdasarkan aktivitas listrik otak yang direkam menggunakan perangkat Muse2.  

## 📊 Metodologi  
1. **Pengumpulan Data**  
   - Data EEG diperoleh dari 45 mahasiswa Fakultas Ilmu Komputer Universitas Brawijaya menggunakan perangkat Muse2.  
   - Sinyal EEG direkam dari empat kanal (sensor elektroda).  

2. **Preprocessing Data**  
   - Filtering menggunakan Butterworth Band-pass Filter.  
   - Zero padding untuk keselarasan panjang sinyal.  
   - Ekstraksi fitur menggunakan Fast Fourier Transform (FFT) dan Discrete Wavelet Transform (DWT).  
   - Labeling data berdasarkan Theta/Beta Ratio dengan metode K-means clustering.  

3. **Model Deep Learning**  
   - Menggunakan kombinasi CNN untuk ekstraksi fitur dan LSTM untuk menangkap pola temporal dari sinyal EEG.  
   - Optimasi hyperparameter dilakukan untuk meningkatkan akurasi model.  

4. **Evaluasi Model**  
   - Menggunakan metrik **precision, recall, F1-score, True Positive Rate (TPR), dan False Positive Rate (FPR)**.  
   - Model dengan FFT memberikan hasil terbaik dengan **precision 0.9878, recall 0.9953, dan F1-score 0.9915**.  

## 🔧 Teknologi yang Digunakan  
- **Python**  
- **TensorFlow/Keras** untuk pembuatan dan pelatihan model CNN-LSTM.  
- **Scikit-Learn** untuk K-means clustering dan evaluasi model.  
- **NumPy & Pandas** untuk pemrosesan data EEG.  
- **Matplotlib & Seaborn** untuk visualisasi hasil klasifikasi.  

## 📂 Struktur Direktori  
```
📁 EEG-Stress-Classification  
│── 📂 Raw_Data_EEG/        # Dataset EEG
│── 📂 Hyperparameter/      # Implementasi Hyperparameter Tuning
│── 1.preprocessing.py      # Skrip untuk preprocessing, FFT, DWT  
│── 2.1 CNN-LSTM_FFT.py     # Implementasi CNN-LSTM FFT  
│── 2.2 CNN-LSTM_DWT.py     # Implementasi CNN-LSTM DWT
│── README.md               # Ringkasan proyek ini  
│── requirements.txt        # Library yang diperlukan  
```  

## 🚀 Cara Menjalankan  
1. Clone repositori ini:  
   ```bash
   git clone https://github.com/username/EEG-Stress-Classification.git
   cd EEG-Stress-Classification
   ```  
2. Install dependensi:  
   ```bash
   pip install -r requirements.txt
   ```  
3. Jalankan preprocessing data:  
   ```bash
   python 1.Preprocessing.py
   ```  
4. Latih model CNN-LSTM FFT:  
   ```bash
   python 2.1.CNN-LSTM_FFT.py
   ```  
5. Latih model CNN-LSTM FFT:    
   ```bash
   python 2.2.CNN-LSTM_DWT.py
   ```  

## 📌 Kesimpulan  
Penelitian ini membuktikan bahwa kombinasi **CNN-LSTM** dengan **FFT** lebih unggul dalam mengklasifikasikan tingkat stres kerja berdasarkan data EEG. Hasilnya dapat digunakan dalam pengembangan sistem pemantauan stres berbasis machine learning.  
