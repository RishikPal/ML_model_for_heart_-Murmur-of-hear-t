# 🔊 Heart Murmur Detection from Audio Signals

This repository contains a Python notebook for detecting heart murmurs from **phonocardiogram (PCG) audio recordings**. The workflow involves signal preprocessing, bandpass filtering, short-term energy computation, and thresholding to identify potential murmur regions within heart sound recordings.

---

## 📖 Overview

Heart murmurs are extra or unusual sounds heard during a heartbeat, often indicating cardiac abnormalities. This notebook automates the murmur detection process by analyzing the energy levels in heart sound recordings within a filtered frequency band (20–200 Hz).

---

## 📂 Project Structure

```

📁 /your\_gdrive\_path/
📁 input/
📄 heart\_sound\_1.wav
📄 heart\_sound\_2.wav
📄 murmur\_extraction.ipynb

````

---

## 🚀 Getting Started

### 📦 Requirements

- Python (via Google Colab)
- Libraries:
  - `librosa`
  - `numpy`
  - `scipy`
  - `matplotlib`

Install missing libraries in Colab:
```python
!pip install librosa matplotlib
````

---

## 📌 How to Run (Step-by-Step)

### 1️⃣ Upload Data to Google Drive

* Upload your heart sound `.wav` files to a folder inside your **Google Drive** (e.g., `/input/`).

### 2️⃣ Open Notebook in Google Colab

* Go to [Google Colab](https://colab.research.google.com/)
* Click **File → Upload Notebook** or **Open from Google Drive**
* Open `murmur_extraction.ipynb`

### 3️⃣ Mount Google Drive

In the first code cell:

```python
from google.colab import drive
drive.mount('/content/drive')
```

Authorize access when prompted.

### 4️⃣ Set File Path and Constants

Specify your folder and parameters:

```python
FOLDER = "/content/drive/MyDrive/your_folder/input/"
SR = 4000
DURATION = 15
```

---

## 📊 Workflow Overview

### 📌 Bandpass Filtering

* Isolates heart sound components between **20 Hz and 200 Hz**.

### 📌 Energy Computation

* Splits signal into short windows.
* Computes signal energy for each window.

### 📌 Murmur Detection

* Thresholds energy values to identify regions with possible murmurs.
* Visualizes murmur regions over time.

---

## 📈 Example Visual Output

* Plot of the filtered signal.
* Energy plot over time.
* Highlighted murmur regions.

---

## 📚 Reference

Basic murmur detection techniques using:

* **Bandpass filtering**
* **Short-term energy analysis**

Inspired by biomedical signal processing principles.

---

## 📜 License

This project is open-source under the **MIT License**.

---

