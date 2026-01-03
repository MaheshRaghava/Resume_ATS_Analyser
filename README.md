# ATS Resume Score Analyser

An AI-powered Applicant Tracking System (ATS) analyzer that evaluates resumes against job descriptions using Google Gemini AI.

## 📋 Overview

The ATS Resume Score Checker helps job seekers optimize their resumes by analyzing how well they match specific job descriptions. Using advanced AI, it provides detailed feedback on matching skills, missing keywords, and suggestions for improvement.

## ✨ Features

- **📄 PDF Resume Processing**: Extract text from uploaded PDF resumes
- **🤖 AI-Powered Analysis**: Uses Google Gemini AI for intelligent matching
- **🎯 Match Score Calculation**: Get a percentage score of resume-JD compatibility
- **🔍 Skills Gap Analysis**: Identify missing and matching skills
- **📊 Detailed Recommendations**: Receive actionable suggestions for improvement
- **🎨 Clean Modern UI**: Responsive design with intuitive interface
- **⚡ Fast Processing**: Quick analysis with real-time results

## 🛠️ Technology Stack

### Backend
- **Python 3.8+** - Core programming language
- **Flask** - Web framework
- **Google Gemini AI** - AI analysis engine
- **PyPDF2** - PDF text extraction
- **Flask-CORS** - Cross-origin support

### Frontend
- **HTML5** - Structure
- **CSS3** - Styling with custom animations
- **JavaScript (ES6+)** - Client-side logic
- **Font Awesome** - Icons
- **Google Fonts (Inter)** - Typography

## 📁 Project Structure

```
Resume_ATS_Analyser/
├── uploads/           # Temporary folder for PDF processing
├── .env              # Environment variables (API keys)
├── .gitignore        # Git ignore rules
├── app.py            # Flask backend & AI integration
├── index.html        # Main frontend interface
├── requirements.txt  # Python dependencies
├── script.js         # Frontend logic & API calls
└── style.css         # Custom styling & animations
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- Google Gemini API key

### Installation

1. **Navigate to project directory**
   ```bash
   cd Resume_ATS_Analyser
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure your API key**
   - Open `.env` file
   - Replace the placeholder with your Gemini API key:
     ```
     GEMINI_API_KEY=your_actual_api_key_here
     DEMO_MODE=false
     ```
   - Get a free API key from [Google AI Studio](https://aistudio.google.com/apikey)

4. **Run the application**
   ```bash
   python app.py
   ```

5. **Access the application**
   - Open your browser
   - Navigate to: `http://127.0.0.1:8080`

## 📖 How to Use

1. **Prepare Your Documents**
   - Have your resume ready as a PDF file
   - Copy the job description you want to apply for

2. **Upload Resume**
   - Click on the upload area or browse to select your PDF resume
   - Maximum file size: 10MB

3. **Paste Job Description**
   - Copy and paste the complete job description
   - Minimum 50 characters required

4. **Analyze**
   - Click "Analyze Resume" button
   - Wait for AI processing (usually 10-30 seconds)

5. **Review Results**
   - View your ATS match score percentage
   - Check matched and missing skills
   - Read detailed AI recommendations
   - Use suggestions to improve your resume

## 🔧 Configuration

### Environment Variables (`.env`)
```env
GEMINI_API_KEY=your_gemini_api_key_here
DEMO_MODE=false  # Set to "true" if API quota is exceeded
```

### Server Settings (`app.py`)
- **Port**: 8080 (change in `app.run()`)
- **Upload Limit**: 10MB
- **Allowed Extensions**: PDF only
- **Upload Folder**: `uploads/` (auto-created)

## 🔒 Security Notes

- API keys are stored in `.env` file (excluded from Git)
- Uploaded files are automatically deleted after processing
- File names are sanitized to prevent path traversal
- File size limits prevent DoS attacks

## ❓ Troubleshooting

### Common Issues

**"API Quota Exceeded" Error**
- Solution 1: Get a new API key from Google AI Studio
- Solution 2: Wait 24 hours for quota reset
- Solution 3: Set `DEMO_MODE=true` in `.env` for testing

**"Could not extract text from PDF"**
- Ensure PDF is text-based (not scanned images)
- Try recreating the PDF from original document
- Check if PDF is password-protected

**"Connection Failed" Error**
- Make sure Flask server is running (`python app.py`)
- Check if port 8080 is available
- Verify firewall isn't blocking the connection

**File Upload Issues**
- Ensure file is under 10MB
- Only PDF files are supported
- Try a different PDF file

## 📈 Features in Detail

### AI Analysis Includes
- **Skills Matching**: Identifies common skills between resume and JD
- **Experience Evaluation**: Assesses years and relevance of experience
- **Education Alignment**: Checks educational qualifications
- **Tools & Technologies**: Compares technical tools mentioned
- **Keyword Optimization**: Suggests important keywords to add
- **Strength Identification**: Highlights resume strong points
- **Improvement Areas**: Provides specific suggestions

### Demo Mode
If `DEMO_MODE=true` in `.env`, the app uses sample data instead of calling the Gemini API. Useful for:
- Testing without API key
- When API quota is exceeded
- Demonstrating functionality offline

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit changes (`git commit -m 'Add some improvement'`)
4. Push to branch (`git push origin feature/improvement`)
5. Open a Pull Request

## 📄 License

This project uses the Apache License 2.0. See the LICENSE file for details.

## 🙏 Credits

- **Google Gemini AI** for powerful language processing
- **Flask Team** for the excellent web framework
- **Font Awesome** for beautiful icons
- **Inter Font** for clean typography

## 📞 Support

For issues or questions:
1. Check the troubleshooting section above
2. Ensure all dependencies are installed
3. Verify your API key is valid
4. Check console for error messages

---
