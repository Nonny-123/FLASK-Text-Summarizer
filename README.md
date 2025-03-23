Flask Text Summarizer

This project is a simple Flask-based API that uses the facebook/bart-large-cnn model from Hugging Face's Transformers library to summarize long pieces of text. The API receives text input via a POST request and returns a summarized version.

📌 Table of Contents

Installation

Usage

Example Request

Technologies Used

Contributing

License

⚙️ Installation

Clone the repository:

    git clone https://github.com/Nonny-123/FLASK-Text-Summarizer.git
    cd FLASK-Text-Summarizer

Create a virtual environment (optional but recommended):

    python -m venv venv
    source venv/bin/activate  # On Windows use: venv\Scripts\activate

Install dependencies:

    pip install -r requirements.txt

Run the Flask App:

    python flask_summarizer.py

The app will be running locally at:

http://0.0.0.0:5000

🚀 Usage

Make a POST request to the /summarizer endpoint with the following JSON payload:

{
  "text": "Your long text here",
  "max_length": 250,
  "min_length": 200
}

Example Request (Python):

import requests

url = 'http://0.0.0.0:5000/summarizer'
data = {"text": "Your long text here", "max_length": 250, "min_length": 200}
response = requests.post(url, json=data)
print(response.json())

Example Response:

{
  "summary": "Summarized text will appear here."
}

🏠 Technologies Used

Python 3.11.1 🐍

Flask 🌐

Transformers 🤗

Requests 📡

🤝 Contributing

Contributions are welcome! Feel free to fork the repo, create a new branch, and submit a pull request.

📄 License

This project is licensed under the MIT License.

👨‍💻 Developed by Okonji Chukwunonyelim Gabriel.

