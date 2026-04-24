<div align="center">

# 🌾 PadiGuard
### Track 1: Agrotechnology
**Strengthening food security through intelligent diagnostics**

[![Live Demo](https://img.shields.io/badge/Live_App-Demo-green?style=for-the-badge&logo=google-cloud)](https://studio--studio-2294378123-a7b3c.us-central1.hosted.app/)
[![Video Demo](https://img.shields.io/badge/Video-Demo-red?style=for-the-badge&logo=youtube)](https://drive.google.com/file/d/1x6Vxu-rPf173h00hGaYLr9_ebMPEJExc/view?usp=sharing)

</div>

---

## ℹ️ Project Overview
**PadiGuard** is an agentic AI solution designed to protect Malaysia’s rice crops. By focusing on early detection of diseases like Blast, Brown Spot, and BLB, we empower farmers to take immediate action, reducing yield loss and supporting national food sovereignty.

## 🚀 Key Features
* **Multimodal Diagnosis:** Uses Gemini 2.0 Flash to "see" and identify leaf pathogens.
* **Grounded Intelligence:** Verified against MARDI research via Vertex AI Search (RAG).
* **Agentic Action:** Automatically suggests treatment plans and local supply resources.

## 🛠️ Tech Stack
* **AI:** Google Gemini 2.0 Flash (Vertex AI)
* **Search/RAG:** Vertex AI Search
* **Hosting:** Firebase & Google Cloud




# 🌾 PadiGuard - AI Rice Disease Detector

**PadiGuard** detects rice plant diseases from leaf photos using Google Gemini AI. Built for Project 2030 Hackathon - Track 1: Padi & Plates.

## 🚀 Live API
```
https://farmleaf-api123-672762415207.us-central1.run.app/predict
```

## 📋 What It Does
- Identifies Rice Blast and Bacterial Leaf Blight from leaf photos
- Returns confidence score (90-95%) and severity level (Low/Medium/High)
- Provides organic + chemical treatment recommendations
- Triggers automatic email alerts based on severity

## 🛠️ Tech Stack
- **Google Gemini 2.0** - AI disease detection
- **Google Cloud Run** - API deployment
- **Python + FastAPI** - Backend framework

## 📡 API Usage

### Endpoint
`POST /predict`

### Form Fields
| Field | Type | Required |
|-------|------|----------|
| firstName | text | Yes |
| lastName | text | Yes |
| email | text | Yes |
| phone | text | Yes |
| file | image | Yes |
| description | text | No |

### Example Request
```bash
curl -X POST https://farmleaf-api123-672762415207.us-central1.run.app/predict \
  -F "firstName=Test" \
  -F "lastName=User" \
  -F "email=test@example.com" \
  -F "phone=123456789" \
  -F "file=@leaf.jpg"
```

### Example Response
```json
{
  "success": true,
  "diagnosis": {
    "disease": "Rice Blast",
    "confidence": "95%",
    "severity": "Medium"
  },
  "treatment": {
    "organic": ["Apply neem oil", "Remove infected leaves"],
    "chemical": ["Apply Tricyclazole"]
  },
  "action_taken": {
    "action": "email_sent",
    "recipient": "farmer@example.com"
  }
}
```

## 🧠 How It Works
```
Leaf photo → Gemini AI → Disease detected → Severity check → Email alert
```

## 📅 Hackathon
**Project 2030: MyAI Future Hackathon** - Advancing the Nation, Building Solutions with Google AI.
```
