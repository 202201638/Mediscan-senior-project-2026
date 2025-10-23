

# 🩺 MediScan AI – Smart Pneumonia Diagnosis System

MediScan AI is an intelligent web and mobile application designed to assist healthcare professionals in detecting pneumonia from chest X-ray images using **Artificial Intelligence (AI)**.  
It provides **automated diagnosis**, **confidence scoring**, and **visual explanations** through heatmaps, enabling faster and more reliable medical decisions.

---

## 🚀 Key Features

- 🧠 **AI-Powered Diagnosis:** Detects pneumonia from chest X-rays using CNN-based deep learning models (DenseNet121 / ResNet50).
- 💡 **Confidence Score:** Displays the model’s confidence percentage for each prediction.
- 🔥 **Explainability (Grad-CAM):** Generates heatmaps highlighting abnormal lung regions.
- 📊 **Doctor Dashboard:** Provides real-time statistics and analysis summaries.
- 📁 **Patient Record Tracking:** Maintains historical scans for comparison and disease progression monitoring.
- 🧾 **PDF Report Generation:** Automatically generates downloadable reports for each diagnosis.
- 👨‍⚕️ **Admin Panel:** Allows administrators to manage doctors, monitor AI performance, and maintain system updates.

---

## 🧩 System Architecture

MediScan AI follows a **modular three-tier architecture** for scalability, performance, and security:

### 1️⃣ Presentation Layer (Frontend)
- Built with **React.js / Next.js / Flutter**
- Features responsive UI for web and mobile
- Handles authentication, image upload, and results visualization

### 2️⃣ Application Layer (Backend)
- Powered by **Flask** or **FastAPI (Python)**
- Manages APIs, authentication (JWT), and communication with AI models
- Handles report generation and data exchange

### 3️⃣ AI Engine (Model Server)
- Uses **TensorFlow / PyTorch** for CNN-based pneumonia detection
- Generates predictions, confidence scores, and Grad-CAM visualizations

### 4️⃣ Data Layer
- **Database:** PostgreSQL / MongoDB  
- **Storage:** AWS S3 / Google Cloud Storage  
- Stores user data, patient history, and AI outputs securely

---

## 🧬 AI Model Workflow

1️⃣ **Image Upload**  
Doctor uploads a chest X-ray image (JPG, PNG, or DICOM).

2️⃣ **Preprocessing**  
Image is resized, normalized, and enhanced for model compatibility.

3️⃣ **Model Inference**  
CNN model (DenseNet121 / EfficientNetB0) predicts *Healthy* or *Pneumonia Detected*.

4️⃣ **Result Generation**  
Outputs include:
- Diagnosis label  
- Confidence score  
- Grad-CAM heatmap  

5️⃣ **Report Creation**  
System generates a structured **PDF report** including:
- Diagnosis result  
- Confidence percentage  
- AI heatmap overlay  
- Doctor’s name and timestamp  

6️⃣ **Data Storage**  
All results are saved in the database for tracking and comparison.

---

## 📂 Datasets

| Dataset | Source | Images | Classes | Link |
|----------|---------|---------|----------|------|
| **NIH ChestX-ray14** | NIH Clinical Center, USA | 112,120 | 14 disease categories | [🔗 Kaggle Link](https://www.kaggle.com/datasets/ammarkhanjadoon/chest-xray-14-dataset) |
| **Chest X-Ray (Pneumonia)** | Kaggle | 5,863 | Normal / Pneumonia | [🔗 Kaggle Link](https://www.kaggle.com/datasets/habibmrad1983/chestxray8-dataset) |

---

## 🧠 Model Performance

| Model | Type | Accuracy | Precision | Recall | F1-Score |
|--------|------|-----------|------------|----------|-----------|
| DenseNet121 | CNN | 94–96% | 93% | 95% | 94% |
| EfficientNetB0 | CNN | 92–94% | 91% | 92% | 91.5% |

---

## 🧰 Tech Stack

| Layer | Technology | Purpose |
|--------|-------------|----------|
| **Frontend** | React.js / Next.js / Flutter | UI and interactivity |
| **Backend** | Flask / FastAPI (Python) | Business logic & APIs |
| **AI Framework** | TensorFlow / PyTorch | Deep learning models |
| **Database** | PostgreSQL / MongoDB | Data management |
| **Storage** | AWS S3 / GCP Storage | Secure image storage |
| **Auth** | JWT | User authentication |
| **Visualization** | Grad-CAM, OpenCV | Explainable AI |
| **Report Generation** | ReportLab / FPDF | PDF diagnostics |
| **Deployment** | Docker / Kubernetes / AWS EC2 | Scalable deployment |

---

## 🧩 Additional Components

### 🧮 Machine Learning (ML)
- Predicts patient recovery trends and pneumonia recurrence using **Random Forest** or **Logistic Regression**.

### 🧠 Deep Learning (DL)
- CNN-based image classification using **DenseNet121** / **EfficientNetB0** for pneumonia detection.

### 💬 Natural Language Processing (NLP)
- Automatically generates readable diagnosis reports using **T5 / BERT / GPT-like** models.
- Supports chatbot-style doctor query assistance for explainability.

---

## 🧑‍💻 Use Cases

| ID | Use Case | Actor | Description |
|----|-----------|--------|-------------|
| UC1 | Doctor Registration & Login | Doctor | Secure access to the platform |
| UC2 | Upload X-ray | Doctor | Upload image for analysis |
| UC3 | AI Diagnosis | Doctor, AI | AI processes and returns results |
| UC4 | Download Report | Doctor | PDF report generation |
| UC5 | Patient History | Doctor | View and compare historical scans |
| UC6 | Manage System | Admin | Manage doctors and monitor AI metrics |

---

## 🧾 User Stories

| ID | Role | Description | Acceptance Criteria |
|----|------|--------------|----------------------|
| US1 | Doctor | Create account & log in | Email verification & secure login |
| US2 | Doctor | Upload chest X-rays | Accepts JPG, PNG, DICOM |
| US3 | Doctor | View confidence score | Displays numeric reliability |
| US4 | Doctor | Download reports | Generates PDF file |
| US5 | Doctor | Compare scans | Displays progress tracking |
| US6 | Admin | Monitor users | Access analytics dashboard |

---

## 🖼️ UI / UX Design

Designed for clarity and clinical usability.  
You can explore the complete UI mockup here:  
🔗 [Visily Design Board](https://app.visily.ai/projects/fb35ea80-f06e-4c4e-9d10-ebd4a9f1793f/boards/2246164)

---

## 🔒 Security & Compliance

- HTTPS and AES encryption for data protection  
- Role-based access control for doctors and admins  
- Secure JWT authentication for sessions  
- GDPR-compliant data handling  

---

## 🧑‍⚕️ Future Enhancements

- Multi-class pneumonia detection (Viral vs Bacterial)  
- Integration with hospital EMR systems  
- Voice-based report generation (NLP)  
- Real-time model monitoring and updates  

---

## 🛠️ Installation (Prototype Setup)

```bash
# Clone repository
git clone https://github.com/yourusername/mediscan-ai.git
cd mediscan-ai

# Backend setup
cd backend
pip install -r requirements.txt
python app.py

# Frontend setup
cd ../frontend
npm install
npm start
````

---

## 🧑‍💻 Contributors

* **[Ahmed Gamal]** – Project Lead & Frontend Engineer & Backend Developer
* **[Sara Mostafa]** – Frontend Engineer & Backend Developer
* **[Habiba Ayman]** – Data Scientist & Ai Engineer 
* **[Moamen Elsharkwy]** – Data Scientist & Ai Engineer 

---

## 📜 License

This project is licensed under the **MIT License** – you are free to use, modify, and distribute with attribution.

---

> 💬 *MediScan AI combines medical imaging and artificial intelligence to support healthcare professionals with faster, more accurate pneumonia diagnosis.*

