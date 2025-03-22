# Prescription OCR App

This Flask-based web application allows users to upload prescription images, extract text using OCR, and retrieve structured medical information, including medication details, dosage, and possible side effects.

## Features
- Upload prescription images (JPG, PNG, etc.).
- Extract patient details, doctor information, prescription date, and medication details.
- Retrieve additional details about medications, including uses and side effects.
- Display extracted data in a structured JSON format.

## Prerequisites
Before running the application, ensure you have the following installed:

- Python 3.x
- Flask
- `pip` (Python package manager)
- Google Generative AI API key (Gemini API)
- Required Python libraries (listed below)

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/exc33ded/ocr-doctor-prescription-reader.git
   cd ocr-doctor-prescription-reader
   ```
2. Create and activate a virtual environment (optional but recommended):
   ```sh
   python -m venv venv
   source venv/bin/activate  # On macOS/Linux
   venv\Scripts\activate     # On Windows
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Set up environment variables:
   - Create a `.env` file in the project root.
   - Add your Google Gemini API key:
     ```env
     GEMINI_API_KEY=your_google_gemini_api_key
     ```

## Running the Application
1. Start the Flask server:
   ```sh
   python app.py
   ```
2. Open a web browser and go to:
   ```
   http://127.0.0.1:5000/
   ```

## Usage
- Upload a prescription image through the web interface.
- The app processes the image using Google Gemini API.
- Extracted details, including patient info and medication data, are displayed on the results page.

## Folder Structure
```
project-directory/
│-- app.py                 # Main application script
│-- templates/
│   ├── index.html         # Upload page
│   ├── result.html        # Results display page
│-- uploads/               # Stores uploaded images
│-- .env                   # Environment variables (API key)
│-- requirements.txt       # List of dependencies
│-- README.md              # Documentation
```

## Dependencies
Make sure you have the following dependencies installed (included in `requirements.txt`):
```txt
Flask
python-dotenv
google-generativeai
```

## Notes
- Ensure that your Google Gemini API key is valid and has the necessary permissions.
- The model currently supports English-language prescriptions.
- The app is running in debug mode; disable debug for production use.

## License
This project is open-source. Feel free to use and modify it as needed.

