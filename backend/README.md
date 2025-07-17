# 👗 GenFit - Virual Try on AI.

![Project Banner](./logo.png)

A cutting-edge, Generative AI-powered virtual try-on web application that enables users to upload a person (model) image and a clothing item image to generate photorealistic try-on previews in seconds. Built using Google Gemini (Generative AI) and FastAPI, this tool delivers high-fidelity outfit visualization with facial identity preservation and seamless garment rendering—perfect for fashion tech, e-commerce, and virtual fitting room experiences.

## 🌟 Key Features

- **Photorealistic Virtual Try-On** - Generate AI-based try-on images with high fidelity
- **Identity Preservation** - Maintains facial features and body proportions
- **Garment Accuracy** - Preserves texture, patterns, and details of clothing items
- **Smart Backgrounds** - Automatically removes and replaces backgrounds
- **Session History** - View and save previous try-on results during your session
- **Responsive UI** - Works seamlessly across devices with dark/light mode support
- **Customization Options** - Control style, garment type, and other parameters

## 🛠️ Technology Stack

### Frontend
- **React.js** - Core framework
- **Ant Design** - UI components and layout
- **Axios** - API communication
- **React Toastify** - Notifications
- **CSS Modules** - Styling

### Backend
- **FastAPI** - REST API framework
- **Uvicorn** - ASGI server
- **Pydantic** - Data validation
- **Python 3.12+** - Backend logic

### AI & Processing
- **Google Gemini API** - Generative AI core
- **Multimodal Processing** - Image-to-image generation
- **Base64 Handling** - Image encoding/decoding

## 🚀 Getting Started

### Prerequisites
- Node.js (v18+)
- Python (3.12+)
- Poetry (for Python dependency management)
- Google Gemini API key

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/abhijeetrogye/genfit.git
   cd genfit

2. **Backend Setup**

    ```bash
    cd backend
    poetry install
    poetry shell

3. **Create .env file:**

    ```ini
    GEMINI_API_KEY=your_actual_gemini_api_key

4. **Run backend:**
    ```bash
    uvicorn main:app --reload

5. **Frontend Setup**
    ```bash
    cd ../frontend
    npm install
    npm run dev

The application will be available at http://localhost:3000 with the API running on http://localhost:8000.

📚 Documentation
API Endpoints
POST /api/try-on

Accepts multipart form data with:

person_image: Model image (JPEG/PNG)

cloth_image: Clothing item image (JPEG/PNG)

Optional parameters:

instructions: Custom prompts

model_type: Body type

gender: Male/Female/Other

style: Clothing style

garment_type: Top/Bottom/Dress etc.

Response Format

json

{
  "status": "success",
  "generated_image": "base64_encoded_image",
  "metadata": {
    "processing_time": 2.45,
    "garment_type": "dress",
    "model_attributes": {...}
  }
}

📂 Project Structure
text
genfit/
├── backend/
│   ├── main.py            # FastAPI application
│   ├── utils/             # Helper functions
│   ├── .env               # Environment variables
│   └── poetry.lock        # Dependency lock file
│
├── frontend/
│   ├── public/            # Static assets
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── pages/         # Application views
│   │   ├── services/      # API services
│   │   └── styles/        # CSS modules
│   └── package.json       # Frontend dependencies
│
├── screenshots/           # Application screenshots
└── README.md              # This document

🤝 Contributing
We welcome contributions! Please follow these steps:

Fork the repository

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

✨ Contributors
<table> <tr> <td align="center"> <a href="https://github.com/abhijeetrogye"> <img src="https://avatars.githubusercontent.com/u/your_avatar" width="100px;" alt="Abhijeet Rogye"/> <br /> <sub><b>Abhijeet Rogye</b></sub> </a> <br /> <span>Lead Developer & Gen AI</span> </td> <td align="center"> <a href="https://github.com/AryaKurup16"> <img src="https://avatars.githubusercontent.com/u/your_avatar" width="100px;" alt="Arya Kurup"/> <br /> <sub><b>Arya Kurup</b></sub> </a> <br /> <span>Backend Developer</span> </td> <td align="center"> <a href="https://github.com/virajtamhanekar"> <img src="https://avatars.githubusercontent.com/u/your_avatar" width="100px;" alt="Viraj Tamhanekar"/> <br /> <sub><b>Viraj Tamhanekar</b></sub> </a> <br /> <span>Frontend Developer</span> </td> </tr> </table>

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments
Google Gemini team for the powerful generative AI API

Ant Design for the beautiful UI components

FastAPI community for the excellent web framework