Project title : PadiGuard 

#Track 1 
Agrotechnology: Strengthening food security through intelligent diagnostics

Live Demo Link : 
Video Demo :

PadiGuard is an intelligent, agentic bio-security platform designed to safeguard Malaysia’s rice sovereignty. As of 2026, Malaysia’s Rice Self-Sufficiency Level (SSL) remains stagnant at ~52%, leaving the nation vulnerable to global supply chain shocks. One of the primary drivers of this deficit is an estimated RM 10 Billion annual loss due to undetected crop pathologies.
Smallholder farmers often lack immediate access to plant pathologists, leading to a "Diagnostic Gap" where diseases are identified only after the damage is irreversible. PadiGuard AI closes this gap by providing every farmer with a 24/7, MARDI-grounded expert diagnostic agent in their pocket

Solution 

# 🌾 Padi Guard - AI Rice Disease Detector

**FarmLeaf** detects rice plant diseases from leaf photos using Google Gemini AI. Built for Project 2030 Hackathon - Track 1: Padi & Plates.

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

## 👥 Team
| Role | Member |
|------|--------|
| AI Prompt & Disease Rules | Person 1 |
| API & Cloud Deployment | Person 2 |
| Frontend (Firebase Studio) | Person 3 |

## 📅 Hackathon
**Project 2030: MyAI Future Hackathon** - Advancing the Nation, Building Solutions with Google AI.
```
