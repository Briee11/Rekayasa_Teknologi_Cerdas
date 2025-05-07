 **prediksi diabetes**

Kelompok: Kelompok 4 Prediksi Diabetes 
Supervisor: Ahmad Radhy, S.Si., M.Si 
Departemen dan Institut: Teknik Instrumentasi, Institut Teknologi Sepuluh Nopember 

Anggota Kelompok :
1. Achmad Fernanda Pramudya Wardhana
2. Meysa Dwidianti
3. Muhammad Zidane Abri Fadhillah Husain

**Description Proyek**
Description Proyek ini terdiri dari beberapa modul berbasis Rust yang digunakan untuk melakukan prediksi diabetes pada cabai berdasarkan beberapa parameter diabetes menggunakan algoritma Neural Network, SVM, dan k-Nearest Neighbor (kNN). Beberapa modul terintegrasi dengan Qt sebagai interface.

**Dataset**
Dataset diambil dari kaggle https://www.kaggle.com/datasets/akshaydattatraykhare/diabetes-dataset

**Struktur Proyek**
Struktur Proyek lookupTable/: Program lookup sederhana untuk konversi nilai. deret taylor/: Proyek perhitungan nilai sudut sinus dan cosinus. svmnkn/: Program prediksi diabetes menggunakan SVM dan kNN. Hasil prediksi divisualisasi dalam .png. nnqt/: Neural Network + integrasi Qt GUI. Meliputi pelatihan model, simpan model (model.bin), dan prediksi.

**Cara Menjalankan Proyek Rust** 

**1. Deret Taylor**
Download file ZIP berjudul taylor.zip.
Buka terminal di folder hasil extract.
Jalankan perintah: code . File > Open Folder > Pilih folder hasil extract
Jalankan program: cargo build -> cargo run

**2. Lookup Table**
Download file ZIP berjudul lookuptable.zip.
Simpan dan extract
Buka terminal di folder hasil extract.
Jalankan perintah: code . File > Open Folder > Pilih folder hasil extract
Jalankan program: cargo build -> cargo run

**3. SVM-KNN**

Download file ZIP berjudul svmknn.zip.
Simpan dan extract
Buka terminal di folder hasil extract.
Jalankan: code . File > Open Folder > Pilih folder hasil extract
Jalankan program dari terminal: cargo build -> cargo run

**4. Neural Network + Frontend QT (nnqt) Step Organize the Project Files**
Create the Project Directory: mkdir soilqt -> cd soilqt
Set Up the Rust Backend: cargo new soilqt -> cd soilqt
Edit the Cargo.toml file to match the provided file
Create the source files in the src directory: touch src/main.rs - touch srcmodel.rs - touch srcdata.rs - touch srcutils.rs
Set Up the Python Frontend: touch qt.py

**Prepare a Sample CSV File:**
The program expects a CSV file with at least 5 columns: 4 features (e.g., temperature, humidity, pH, moisture) and 1 label (0 or 1 for soil fertility).
Create a sample CSV file named soil_data.csv in the soilqt_project directory:
Step Build the Rust Backend

**Navigate to the Rust Project Directory: cd soilqt**
Build the Rust Binary in Release Mode: The Python frontend expects the compiled binary at ./target/release/soilqt. Run: cargo build --release
Verify the Build: Ensure the binary exists: ls target/release/soilqt Test the binary with a training command (optional): ./target/release/soilqt --train ../soil_data.csv 100 0.01 This should load the CSV, train the model, and generate model.bin, scaler.bin, results.json, and plots in the output directory.
Step Run the Python GUI

**Ensure the Rust Binary Exists:** 
The Python script (qt.py) calls the Rust binary (./target/release/soilqt) for training and prediction. Ensure the binary is built (from Step 3). 2.If using a virtual environment, activate it first: source venv/bin/activate

**Run the Python Script:** 
In the soilqt_project directory, run: python3 qt.py This should launch the PyQt5 GUI window titled "Soil Fertility Predictor".
Interact with the GUI: Load CSV: Click "Browse" to select soil_data.csv or enter its path manually. Click "Load Data". The status bar should update to show the number of data points loaded (e.g., "Status: Loaded 5 points"). Train the Model: Set "Epochs" (e.g., 1000) and "Learning Rate" (e.g., 0.001). Click "Train Model". The GUI will display training progress (epoch, loss, accuracy) and update the plot in real-time. After training, the status bar will show validation and test accuracy, and the table will display predictions for 5 random test points. Make Manual Predictions: Enter values for Temperature, Humidity, Soil pH, and Moisture (e.g., 25.0, 60.0, 6.5, 30.0). Click "Predict". The result will appear next to the button (e.g., "Prediction: Fertile (Probability: 0.750)"). Handle Errors: If you try to predict without training, the GUI will show an error: "Train a model first to generate model.bin and scaler.bin!". Invalid inputs (e.g., non-numeric values) will trigger appropriate error messages.

**Persyaratan**
- Instal Rust: curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh.
- Instal dependensi tambahan sesuai file di Cargo.toml.
- Pastikan Python dan PyQt terinstal untuk Qt_Rust.rs.
- Install System Dependencies : sudo apt install libxkbcommon-x11-0 libxcb-icccm4 libxcb-image0 libxcb-keysyms1 libxcb-randr0 libxcb-render-util0 libxcb-xinerama0 qt5-default Note: If qt5-default is unavailable (e.g., Ubuntu 20.04+), install: sudo apt install libqt5widgets5 libqt5gui5 libqt5core5a
- Install Python Dependencies : pip3 install pyqt5 matplotlib numpy
- Optional: Use a virtual environment to avoid conflicts: python3 -m venv venv source venv/bin/activate pip install pyqt5 matplotlib numpy
