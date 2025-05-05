# Rekayasa_Teknologi_Cerdas

Berikut adalah tata cara penjelasan pembuatan file dengan implementasi menggunakan Rust dan Qt:


# Proyek Rust untuk Algoritma dan Antarmuka

Repositori ini berisi lima file yang dikembangkan menggunakan Rust untuk berbagai implementasi algoritma dan satu file yang mengintegrasikan Rust dengan Qt untuk antarmuka grafis.

# Tata Cara Pembuatan File 

Data Sets : https://www.kaggle.com/datasets/akshaydattatraykhare/diabetes-dataset

Pregnancies: To express the Number of pregnancies
Glucose: To express the Glucose level in blood
BloodPressure: To express the Blood pressure measurement
SkinThickness: To express the thickness of the skin
Insulin: To express the Insulin level in blood
BMI: To express the Body mass index
DiabetesPedigreeFunction: To express the Diabetes percentage
Age: To express the age
Outcome: To express the final result 1 is Yes and 0 is No

## Tata Cara Pembuatan File 

1. **deret_taylor.rs**  
   File ini berisi implementasi Deret Taylor dalam Rust untuk menghitung aproksimasi fungsi matematis seperti sin(x) atau cos(x) menggunakan deret tak hingga.  
   - **Langkah Pembuatan**: Tulis kode Rust untuk menghitung Deret Taylor, uji dengan input berbeda, dan simpan sebagai `deret_taylor.rs`.  
   - **Dependensi**: Pastikan Rust dan Cargo terinstal.  
   - **Cara Jalankan**: Kompilasi dengan `cargo run --release --bin deret_taylor`.

2. **lookup_table.rs**  
   File ini mengimplementasikan tabel pencarian (lookup table) dalam Rust untuk menyimpan dan mengakses data pra-dihitung secara efisien.  
   - **Langkah Pembuatan**: Buat struktur data untuk tabel, isi dengan nilai awal, dan tambahkan fungsi pencarian, simpan sebagai `lookup_table.rs`.  
   - **Dependensi**: Rust dan Cargo.  
   - **Cara Jalankan**: Kompilasi dengan `cargo run --release --bin lookup_table`.

3. **svm_knn_diabetes.rs**  
   File ini menggabungkan algoritma SVM dan KNN dalam Rust untuk klasifikasi dataset diabetes.  
   - **Langkah Pembuatan**: Implementasikan logika SVM dan KNN, integrasikan dengan library Rust seperti `linfa`, dan simpan sebagai `svm_knn_diabetes.rs`.  
   - **Dependensi**: Tambahkan `linfa` dan `ndarray` di `Cargo.toml`.  
   - **Cara Jalankan**: Kompilasi dengan `cargo run --release --bin svm_knn_diabetes`.

4. **NN_diabetes.rs**  
   File ini berisi implementasi Neural Network dalam Rust untuk prediksi diabetes berdasarkan dataset.  
   - **Langkah Pembuatan**: Gunakan library seperti `tch-rs` untuk jaringan saraf, latih model dengan data diabetes, dan simpan sebagai `NN_diabetes.rs`.  
   - **Dependensi**: Instal `tch-rs` dan tambahkan ke `Cargo.toml`.  
   - **Cara Jalankan**: Kompilasi dengan `cargo run --release --bin NN_diabetes`.

5. **Qt_Rust.rs**  
   File ini mengintegrasikan Rust dengan Qt menggunakan `qt.py` untuk membangun antarmuka grafis.  
   - **Langkah Pembuatan**: Instal `qt.py`, tulis kode Rust untuk logika, hubungkan dengan antarmuka Qt, dan simpan sebagai `Qt_Rust.rs`.  
   - **Dependensi**: Rust, Cargo, dan `qt.py` (pastikan Python dan PyQt terinstal).  
   - **Cara Jalankan**: Kompilasi Rust dengan `cargo build`, lalu jalankan dengan `python -m qt.py Qt_Rust.rs`.

## Persyaratan
- Instal Rust: `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`.
- Instal dependensi tambahan sesuai file di `Cargo.toml`.
- Pastikan Python dan PyQt terinstal untuk `Qt_Rust.rs`.
