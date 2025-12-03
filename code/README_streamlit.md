# Fraud Detection Streamlit App

A simple web interface for the BERT + XGBoost fraud detection system with AI-powered explanations.

## Features

- **Text Input**: Enter suspicious text for analysis
- **Real-time Classification**: Get instant fraud type predictions
- **Confidence Scores**: See prediction confidence levels
- **All Class Probabilities**: View probabilities for all fraud types
- **AI Explanations**: Get detailed explanations using OpenAI GPT-3.5
- **Example Texts**: Try pre-loaded examples of different fraud types

## Setup

1. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

2. **Environment Setup**:
   - Make sure your `.env` file is in the `code/` folder with your OpenAI API key:
   ```
   API_KEY=your_openai_api_key_here
   ```

3. **Run the App**:
   ```bash
   streamlit run fraud_detection_app.py
   ```

## How It Works

1. **Text Preprocessing**: Cleans and tokenizes input text using NLTK
2. **BERT Embeddings**: Generates 384-dimensional semantic embeddings using `BAAI/bge-small-en-v1.5`
3. **XGBoost Classification**: Predicts fraud type using trained XGBoost model
4. **AI Explanation**: Uses OpenAI GPT-3.5-turbo to explain the classification

## Usage

1. Enter suspicious text in the text area
2. Click "Analyze for Fraud" to get predictions
3. View the classification result and confidence score
4. Click "Explain Result" to get AI-powered explanations
5. Try the example texts to see different fraud types

## Model Performance

The system can detect multiple fraud types including:
- Lottery scams
- Romance scams 
- Tech support scams
- And more...

## Note

On first run, the app will download NLTK data and load the BERT model, which may take a few moments.
