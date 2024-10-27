# Customer Support AI Chatbot

This project implements an AI-powered customer support chatbot system using Mistral AI.

## Features

- AI-driven intent prediction for customer queries
- Real-time chat interface built with Flet
- Integration with Mistral AI for natural language processing
- Comprehensive evaluation tools for model performance

## Project Structure

- `HFlet/`: Frontend application using Flet
  - `main.py`: Entry point for the Flet application
  - `presentation/`: UI components and presenters
  - `domain/`: Business logic and data models
- `HService/`: Backend service and AI processing
  - `api_dialogue.py`: FastAPI server for dialogue processing
  - `domain/`: Core dialogue management and intent prediction
  - `add_predictions.py`: Script for adding predictions to the dataset
  - `evaluate_predictions.py`: Evaluation script for model performance

## Setup and Installation

1. Clone the repository:
   ```
   git clone https://github.com/HypecatAI/llmhackathon.git
   cd llmhackathon
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory and add your API keys:
   ```
   MISTRAL_API_KEY=your_mistral_api_key_here
   ```

## Running the Application

1. Start the backend service:
   ```
   uvicorn api_dialogue:app HService/api_dialogue.py
   ```

2. Launch the Flet frontend:
   ```
   flet run --web HFlet/main.py
   ```

## Data Processing and Evaluation

- To prepare the dataset:
  ```
  python HService/prepare_dataset.py
  ```

- To add predictions to the dataset:
  ```
  python HService/add_predictions.py
  ```

- To evaluate model performance:
  ```
  python HService/evaluate_predictions.py
  ```

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.
