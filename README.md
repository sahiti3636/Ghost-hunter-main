# 👻 Ghost Hunter: Dark Vessel Detection System

![Ghost Hunter](https://img.shields.io/badge/Status-Active-success)  
![Python](https://img.shields.io/badge/Python-3.12%2B-blue)  
![React](https://img.shields.io/badge/Frontend-React%20%2F%20Next.js-blueviolet)

> **Advanced maritime intelligence system fusing Sentinel-1 SAR imagery with GenAI to detect illicit "dark vessels".**

---

## 🎥 Demo

- 🎥 **System Demo:** https://youtu.be/e0lUgmcCVbU
- **Website Link:** https://ghost-hunter-eta.vercel.app

---

## 📚 Documentation

📄 **Detailed Architecture, Problem Statement & Technical Design**  
👉 https://docs.google.com/document/d/1F8qbUlpY5mmD9qXqkOsk9WE-dmcd-b-PoYVR8xLBuTM/edit?usp=sharing  

We present an end-to-end maritime intelligence system that tackles illegal, unreported, and unregulated (IUU) fishing using satellite radar, computer vision, and behavioral analysis.

Our approach goes beyond simple vessel detection by fusing Sentinel-1 SAR imagery, physics-based ship detection, CNN-based visual validation, AIS silence verification, and context-aware risk scoring to identify dark vessels operating inside protected marine regions.

By combining spatial legality (MPAs), motion cues, fleet-level context, and explainable risk fusion, the system produces actionable, analyst-ready intelligence rather than raw alerts — enabling faster, more informed maritime enforcement decisions.

---

## ⚠️ Deployment & Architecture Note
The provided website link showcases a lightweight version of the full project, designed to give an overall intuition of its functionality. Since deploying the full deep learning–based backend is resource-intensive, this version allows you to explore a subset of regions from the dropdown menu, which have already been thoroughly analyzed by the complete pipeline.

**Why is this not hosted on Vercel/Render?**

Ghost Hunter deals with **high-resolution Synthetic Aperture Radar (SAR) satellite imagery** and runs **complex CNN inference** locally. 

1. **Computational Intensity**: Processing 250MB+ satellite product files requires significant RAM and CPU power, exceeding the limits of standard free-tier PaaS platforms.  
2. **Model Size**: The PyTorch CNN models and geospatial libraries (GDAL/Rasterio) result in a large build size best suited for containerized environments (Docker/Kubernetes) or dedicated compute instances.

**We provide a seamless local setup script to replicate the full production environment on your machine.**

---

## 🚀 Key Features

- **Multi-Source Data Fusion**: Correlates Sentinel-1 SAR imagery with real-time AIS data  
- **Dark Vessel Detection**: Identifies vessels visible in radar but missing from AIS tracking  
- **Risk Assessment**: Assigns risk scores based on behavior, location, and historical patterns  
- **GenAI Intelligence**: Generates automated intelligence reports using Gemini models  
- **Interactive Dashboard**: Next.js frontend for visualizing detections on a map  

---

## 🛠️ Prerequisites

Before you begin, ensure you have:

1. **Python 3.12+** → https://www.python.org/downloads/  
2. **Node.js & npm** → https://nodejs.org/  
3. **Git** → https://git-scm.com/  

---

## ⚡ Quick Start (Automated)

### 🍎 macOS / Linux

```bash
git clone https://github.com/sahiti3636/HackXios-Ghost-Hunter.git
cd HackXios-Ghost-Hunter
chmod +x setup.sh
./setup.sh
```

### 🪟 Windows

```powershell
git clone https://github.com/sahiti3636/HackXios-Ghost-Hunter.git
cd HackXios-Ghost-Hunter
.\setup.ps1
```

---

## 🧰 Manual Setup

### 1. Backend

```bash
python -m venv venv
# Activate venv (source venv/bin/activate OR .\venv\Scripts\Activate)
pip install -r requirements_backend.txt
python app.py
```

### 2. Frontend

```bash
cd ghost-hunter-frontend
npm install
npm run dev
```

---

## 🤝 Contributors

1. https://github.com/varun-iiitb  
2. https://github.com/sahiti3636  
3. https://github.com/navya2208  
4. https://github.com/shivansh-shah  
