# 👗 GenFit – Virtual Try-On AI

![Genfit Banner](frontend/public/logo.png)

A Gen AI-powered virtual try-on web application that allows users to upload a person image and a clothing image to generate photorealistic outfit previews.  
Built with **Google Gemini**, **FastAPI**, and **React**.

---

## 🌟 Features

- **Photorealistic AI Try-On**
- **Facial Identity Preservation**
- **Detailed Garment Rendering**
- **Background Removal & Replacement**
- **Session History Storage**
- **Responsive Dark/Light UI**
- **Customizable Prompts & Styles**

---

## 🛠️ Tech Stack

### 🔹 Frontend
- React.js
- Ant Design
- Axios
- React Toastify
- CSS Modules

### 🔹 Backend
- FastAPI + Uvicorn
- Python 3.12+
- Pydantic

### 🔹 AI Integration
- Google Gemini API
- Multimodal Image Processing
- Base64 Image Encoding/Decoding

---

## 🚀 Local Development Setup

### 🔧 Backend

```bash
cd backend
poetry install
poetry shell
````

Create `.env` file:

```ini
GEMINI_API_KEY=your_gemini_api_key_here
```

Run server:

```bash
uvicorn main:app --reload
```

### 💻 Frontend

```bash
cd frontend
npm install
npm run dev
```

* App: [http://localhost:3000](http://localhost:3000)
* API: [http://localhost:8000](http://localhost:8000)

---

## 📚 API Documentation

### `POST /api/try-on`

**Form Fields:**

| Field         | Type            | Description                |
| ------------- | --------------- | -------------------------- |
| person\_image | Image (jpg/png) | Image of the model/person  |
| cloth\_image  | Image (jpg/png) | Clothing item image        |
| instructions  | Text (optional) | Custom prompt instructions |
| model\_type   | Text (optional) | Body type                  |
| gender        | Text (optional) | Male / Female / Other      |
| style         | Text (optional) | Clothing style             |
| garment\_type | Text (optional) | Top / Bottom / Dress etc.  |

**Response:**

```json
{
  "status": "success",
  "generated_image": "base64_encoded_image",
  "metadata": {
    "processing_time": 2.45,
    "garment_type": "dress",
    "model_attributes": {...}
  }
}
```

---

## 📁 Project Structure

```
genfit/
├── backend/
│   ├── main.py
│   ├── utils/
│   ├── .env
│   └── poetry.lock
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── styles/
│   └── package.json
│
└── README.md
```

---

## 🤝 Contributing

```bash
# Fork the repository
# Create a new feature branch
git checkout -b feature/YourFeature

# Commit your changes
git commit -m "Added new feature"

# Push to GitHub
git push origin feature/YourFeature

# Open a Pull Request
```

---

## ✨ Contributors

* [GitHub – Abhijeet Rogye](https://github.com/abhijeetrogye)
  [LinkedIn – Abhijeet Rogye](https://linkedin.com/in/abhijeetrogye)

* [GitHub – Arya Kurup](https://github.com/AryaKurup16)
  [LinkedIn – Arya Kurup](https://www.linkedin.com/in/arya-kurup-aa7264244/)

* [GitHub – Viraj Tamhanekar](https://github.com/virajtamhanekar)
  [LinkedIn – Viraj Tamhanekar](https://www.linkedin.com/in/viraj-tamhanekar/)

---

## 📄 License

This project is licensed under the **MIT License**.
See the `LICENSE` file for details.

---

## 🙏 Acknowledgments

* Google Gemini – Generative AI API
* Ant Design – UI Components
* FastAPI – Web Backend Framework

