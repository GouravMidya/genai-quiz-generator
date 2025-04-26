# AI Quiz Generator

A Flask-based web service that generates quizzes using Google's Vertex AI platform and the Gemini model.

## Description

This project provides a RESTful API that generates customized quizzes on various topics using Google's Vertex AI generative models. The service allows users to specify the topic, number of questions, difficulty level, and language for the generated quiz.

## Prerequisites

- Python 3.x
- Google Cloud Platform account
- Vertex AI API enabled
- Required environment variables configured

## Installation

1. Clone the repository:
```bash
git clone https://github.com/GouravMidya/genai-quiz-generator.git
cd genai-quiz-generator
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Copy the `.env.sample` file to `.env` and configure your environment variables:
```bash
cp .env.sample .env
```

4. Update the `.env` file with your Google Cloud Platform settings:
```
PORT=8080
PROJECT_ID=your-project-id
PROJECT_LOCATION=your-project-location
MODEL_NAME=your-model-name
```

## Usage

1. Start the server:
```bash
python main.py
```

2. Make GET requests to generate quizzes. Example:
```
http://localhost:8080/?topic=History&num_q=5&diff=intermediate&lang=English
```

### Query Parameters

- `topic` (optional): Quiz topic (default: "History")
- `num_q` (optional): Number of questions (default: 5)
- `diff` (optional): Difficulty level (default: "intermediate")
- `lang` (optional): Language for the quiz (default: "English")

### Response Format

The API returns a JSON array of quiz questions:
```json
[
  {
    "question": "Question text",
    "responses": ["Option 1", "Option 2", "Option 3", "Option 4"],
    "correct": "Correct answer"
  }
]
```

## Environment Variables

- `PORT`: Server port (default: 8080)
- `PROJECT_ID`: Google Cloud Project ID
- `PROJECT_LOCATION`: Google Cloud Project Location
- `MODEL_NAME`: Vertex AI Model Name

## Dependencies

- Flask (3.0.0)
- gunicorn (21.2.0)
- google-cloud-aiplatform (1.47.0)



## Output
![image](https://github.com/user-attachments/assets/173eb47a-c152-49cc-803e-b07098643a88)

![image](https://github.com/user-attachments/assets/9e181539-0470-43ef-9b96-1c3bd1a06397)





