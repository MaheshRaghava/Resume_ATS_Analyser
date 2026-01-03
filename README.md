# Resume_ATS_Analyzer

An **AI-powered ATS Resume Analyzer** built with **Flask** and **Google Gemini AI**. This tool allows you to evaluate resumes against job descriptions, identify missing skills, and get a match score—helpful for job applicants and recruiters alike.

---

## 🚀 Key Features

- **Upload Resumes**: PDF format, max 10MB  
- **AI-Powered Analysis**: Extracts skills, experience, education, and tools  
- **Match Scoring**: Get ATS-style match percentage with recommendations  
- **Skills Gap Detection**: Highlights missing or underrepresented skills  
- **Interactive Results**: Structured output with suggestions for improvement  
- **Real-Time Validation**: Checks inputs and provides error messages  
- **Responsive UI**: Works on desktop and mobile  

---

## 🛠 Technology Stack

- **Backend**: Python 3 + Flask  
- **AI Engine**: Google Gemini 1.5 Flash  
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)  
- **PDF Processing**: PyPDF2  
- **Styling**: Custom CSS & animations  
- **CORS Handling**: `flask-cors`  

---

## ⚡ Installation & Setup

### **1️⃣ Clone the Repository**

```bash
git clone https://github.com/yourusername/ATS_Checker.git
cd ATS_Checker
2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Configure API Key

Edit the .env file and add your Gemini API key:

GEMINI_API_KEY=your_api_key_here
DEMO_MODE=false


Tip: Set DEMO_MODE=true to test without consuming API quota.

4️⃣ Start the Server
python app.py

5️⃣ Open the Application

Navigate to: http://127.0.0.1:8080 in your browser

🎯 How to Use
1️⃣ Upload Resume

Click Upload Resume and select a PDF (text-based, not scanned images)

2️⃣ Enter Job Description

Paste the full job description (minimum 50 characters)

3️⃣ Analyze Resume

Click the Analyze Resume button

Wait for the AI to process the resume and job description

4️⃣ View Results

ATS Match Score: Shows percentage of match

Matched Skills: Skills present in both resume and job description

Missing Keywords: Skills required but missing in resume

Detailed Recommendations: Suggestions to improve your match

5️⃣ Repeat Analysis

Upload a new resume or job description for another evaluation

📂 Project Structure
ATS_Checker/
├── uploads/            # Temporary storage for uploaded PDFs
├── .env                # API key and configuration
├── .gitignore          # Files/folders ignored by Git
├── app.py              # Flask backend + Gemini AI integration
├── index.html          # Frontend interface
├── requirements.txt    # Python dependencies
├── script.js           # Frontend JS logic & API calls
└── style.css           # Custom styling & animations

🔗 API Endpoints
1️⃣ POST /analyze

Purpose: Analyze resume against job description

Request (multipart/form-data):

resume: PDF file

job_description: string

Response: JSON with parsed resume, job description, and ATS match result

2️⃣ GET /health

Purpose: Health check endpoint

Response: JSON with service status

3️⃣ GET /

Purpose: Serves main application page

⚙️ Configuration Options

Maximum Upload Size: 10MB (app.config["MAX_CONTENT_LENGTH"])

Allowed File Types: PDF only (ALLOWED_EXTENSIONS in app.py)

Demo Mode: Set DEMO_MODE=true in .env to bypass Gemini API calls

🛠 Troubleshooting Steps
1️⃣ PDF Extraction Fails

Ensure PDF is text-based, not scanned images

For image-based PDFs, use OCR before uploading

2️⃣ API Key Issues

Confirm .env contains a valid Gemini API key

If API quota exceeded, use DEMO_MODE=true temporarily

3️⃣ Port Conflicts

Change the port in app.py if 8080 is already in use:

app.run(debug=True, port=5000)

4️⃣ Missing Dependencies
pip install -r requirements.txt

📜 License

This project is licensed under the Apache License 2.0 – see the LICENSE file for details.
Apache License 2.0

🙏 Acknowledgements

Built with Flask & Google Gemini AI

Icons from Font Awesome

UI inspired by modern ATS dashboards
