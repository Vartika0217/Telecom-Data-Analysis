# Telecommunication Industry Data Analysis

A data-driven project to filter and identify mobile phones that meet modern user expectations in terms of features, screen quality, camera capabilities, and physical design using a real-world telecom dataset.

---

## Project Overview

This analysis focuses on evaluating smartphones based on:

* Core features (Bluetooth, WiFi, Touch Screen, External Memory)
* Display resolution and screen diagonal size
* Front and rear camera resolution
* Physical attributes like weight and thickness
* Variability across numerical features

Logical filtering and feature engineering were applied to shortlist phones that offer the best overall performance.

---

## Dataset

A dataset containing detailed specifications of multiple smartphone models, including:

* Technical specs (RAM, Storage, Battery, etc.)
* Hardware features (Camera, Resolution, Size, etc.)
* Boolean flags for feature availability (e.g., Bluetooth, WiFi)

---

## Key Techniques Used

### Feature Engineering:

* `Px` = `Px_h * Px_w` → total screen resolution
* `Scr_d` = diagonal length using `sqrt(Scr_h² + Scr_w²)`

###  Logical Filtering:

Applied multiple conditions:

* Must support Bluetooth, WiFi, Touch Screen, and External Memory (`con1`)
* Must have above-median screen resolution (`con_px`)
* Must have large screen size (Scr\_d ≥ Q3) (`con3`)
* Must have both cameras above median resolution (`con_cam`)
* Must have good primary and front camera reso;ution (`con4`)
* Must have good internal memory, battery power and RAM (`con5`)
* Must be slim and light (below median depth and weight) (`con6`)


### ✅ Statistical Profiling:

* Calculated **standard deviation to mean ratio** for all numeric features to assess variability

### ✅ Visualization:

* Histograms for key features: resolution, cameras, screen size, weight, depth
* Overlay of **mean**, **median**, and **quartile** lines for clarity

---

## 📌 Output

* A filtered dataset (`df1`) containing phones that satisfy **all desired conditions**
* Analytical insights into which features contribute most to performance and user satisfaction

---

## 📊 Tools & Libraries

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Google Colab 

---

## 🚀 How to Use

1. Clone this repository
2. Open the notebook in Google Colab or Jupyter
3. Run all cells sequentially
4. Explore filtered phones and modify thresholds as needed

---

## 📬 Contact

For suggestions, feedback, or collaboration:
**\[Vartika Mishra]** – \[www.linkedin.com/in/vartika-mishra-79a75627a] | \[vartikam002@gmail.com]

---

> “Let data guide decisions — not assumptions.”
