# Product-Promo-Generator



---
# 🌟 Banner Creator 🌟

  

### **🚀 Effortlessly design stunning product banners using advanced AI technology.**

  

---

  

## Contents

- [✨ Overview](#-overview)

- [⚙️ Key Features](#%EF%B8%8F-key-features)

- [🛠️ Setup](#%EF%B8%8F-setup)

- [🎮 How to Use](#-how-to-use)

- [🔹 Frontend Usage](#-frontend-usage)

- [🔹 Backend Functionality](#-backend-functionality)

- [⚡ Tools and Technologies](#-tools-and-technologies)

  

---

  

## ✨ Overview

Welcome to the **Banner Creator**, an intuitive platform for crafting visually appealing product banners. Utilizing state-of-the-art **Generative AI models** like **Google Gemini and Google Imagen**, this tool simplifies the banner creation process for maximum efficiency.

  

> 📌 **Note:** Designed for learning and creative experimentation, this project is ideal for designers and marketers seeking to create impressive banners with ease.

  

---

  

## ⚙️ Key Features

- **🖼️ Image Integration**: Easily upload one or more images to include in your banners.

- **📝 Intelligent Content Creation**: Employs generative AI to craft banners based on themes and styles.

- **📐 Versatile Dimensions**: Offers support for various aspect ratios (e.g., 1:1, 16:9).

- **🖍️ Automatic Image Fixes**: Detects and corrects image issues for a polished output.

- **🔍 Real-Time Previews**: View and adjust your uploaded images and generated banners before downloading.

  

---

  

## 🛠️ Setup

  

### Prerequisites

- Python 3.11

- Gemini API Access

- Google Cloud Platform and Vertex AI credentials

- Access to Google Imagen

- Huggingface Account

  

### Installation Steps

1. **Clone the Repository**:


```bash
git clone https://github.com/nik-hil-29/Product-Promo-Generator.git

cd product-banner-generator

```

  

2. **Set Up a Virtual Environment**:

```bash

python -m venv venv

source venv/bin/activate # Use `venv\\Scripts\\activate` on Windows

```

  

3. **Install Required Packages**:

```bash

pip install -r requirements.txt

```

  

4. **Start the Backend (FastAPI)**:

```bash

uvicorn backend:app --host 0.0.0.0 --port 8000 --reload

```

  

5. **Launch the Frontend (Gradio)**:

```bash

python frontend.py

```

  

---

  

## 🎮 How to Use

<b>🔹 Frontend Usage</b>

1. **Open the UI**: Navigate to `http://localhost:8000` in your browser.

2. **Provide Details**: Enter the banner topic, including product details, themes, and colors.

3. **Upload Images**: Use the "📸 Upload Images" option to add images.

4. **Choose Aspect Ratio**: Select a ratio like `1:1` or `16:9` from the dropdown.

5. **Generate Banner**: Click "✨ Generate Banner" to create your banner in under a minute!

  



<b>🔹 Backend Functionality</b>

The backend provides an API for banner generation.

- **Endpoint**: `/generate_banner`

- **Method**: `POST`

- **Parameters**:

  - `topic`: The banner topic (string)

  - `images`: List of uploaded images (file input)

  - `aspect_ratio`: Optional aspect ratio (`1:1`, `9:16`, etc.)

Example API usage via cURL:

```bash

curl -X POST -F "topic=Summer Sale" -F "images=@path/to/image1.jpg" -F "aspect_ratio=16:9" http://localhost:8000/generate_banner

```

  

---

  

## ⚡ Tools and Technologies

- **🖥️ Backend**: FastAPI - A high-performance Python framework.

- **🤖 AI Models**: Google Gemini and Google Imagen via Vertex AI.

- **🎨 Interface**: Gradio - A user-friendly tool for ML model interaction.

- **💾 Storage**: Local storage for banners, with options for GCP buckets.

  

---

  

## 💡 How It Operates

  

1. **Input Collection**: Users specify banner requirements through a Gradio interface.

2. **Processing in the Backend**: FastAPI processes the inputs and invokes the `BannerGenerator` class.

3. **AI-Driven Generation**: The AI models analyze inputs and generate banner designs.

4. **Optimization**: Generated banners are refined for consistency and quality.

5. **Output Display**: The final banners are shown in the UI for preview and download.

  

---
