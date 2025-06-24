# Chatbot-Project
# AI Chatbot Project

A conversational AI chatbot built with Python, Flask, and TensorFlow that uses natural language processing to engage in meaningful conversations with users.

## 🚀 Features

- **Natural Language Processing**: Uses NLTK for text preprocessing and understanding
- **Neural Network Model**: Built with TensorFlow/Keras for intelligent response generation
- **Web Interface**: Flask-based web application with RESTful API
- **Conversational AI**: Handles various conversation types including:
  - Greetings and farewells
  - Questions and clarifications
  - General statements and opinions
  - Agreement/disagreement responses
  - Fallback responses for unrecognized inputs
- **Real-time Chat**: Interactive web interface for seamless conversation
- **CORS Support**: Cross-origin resource sharing enabled for web integration

## 🛠️ Technology Stack

- **Backend**: Python 3.x, Flask
- **AI/ML**: TensorFlow, Keras, NLTK
- **Data Processing**: NumPy, scikit-learn
- **Web**: HTML, CSS, JavaScript
- **Development**: Virtual environment, pip

## 📋 Prerequisites

Before running this project, make sure you have:

- Python 3.7 or higher installed
- pip package manager
- Git (for cloning the repository)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd ChatbotProject
   ```

2. **Create and activate virtual environment**
   ```bash
   # On Windows
   python -m venv venv
   venv\Scripts\activate

   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download NLTK data**
   ```bash
   python download_nltk_data.py
   ```

## 🎯 Usage

1. **Start the application**
   ```bash
   python app.py
   ```

2. **Access the chatbot**
   - Open your web browser
   - Navigate to `http://localhost:5000`
   - Start chatting with the AI!

3. **API Usage**
   The chatbot also provides a REST API endpoint:
   ```bash
   POST /api/chat
   Content-Type: application/json
   
   {
     "message": "Hello, how are you?"
   }
   ```

## 🏗️ Project Structure

```
ChatbotProject/
├── app.py                 # Main Flask application
├── chatbot_model.py       # AI model implementation
├── download_nltk_data.py  # NLTK data download script
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
├── templates/            # HTML templates
└── venv/                # Virtual environment
```

## 🧠 How It Works

### 1. Natural Language Processing
- **Tokenization**: Breaks down user input into individual words
- **Lemmatization**: Reduces words to their base form (e.g., "running" → "run")
- **Bag of Words**: Converts text into numerical vectors for machine learning

### 2. Neural Network Architecture
- **Input Layer**: Processes the bag of words representation
- **Hidden Layers**: 128 and 64 neurons with ReLU activation
- **Dropout Layers**: Prevents overfitting (50% dropout rate)
- **Output Layer**: Softmax activation for intent classification

### 3. Training Process
- **Data Preparation**: Processes intent patterns and responses
- **Model Training**: 200 epochs with SGD optimizer
- **Intent Classification**: Predicts user intent from input
- **Response Generation**: Selects appropriate response from intent

### 4. Conversation Flow
1. User sends message
2. Text is preprocessed (tokenized, lemmatized)
3. Neural network predicts intent
4. Appropriate response is selected and returned
5. Fallback response if intent not recognized

## 🎨 Intent Categories

The chatbot is trained to handle various conversation types:

- **Greeting**: "hi", "hello", "hey", "how are you"
- **Goodbye**: "bye", "see you later", "goodbye"
- **Thanks**: "thank you", "thanks", "i appreciate it"
- **General Questions**: "what", "how", "why", "when", "where"
- **General Statements**: "i think", "i believe", "i feel"
- **Clarification**: "i don't understand", "can you explain"
- **Agreement**: "yes", "sure", "okay", "alright"
- **Disagreement**: "no", "i disagree", "that's not right"
- **Fallback**: Default responses for unrecognized inputs

## 🔧 Configuration

### Model Parameters
- **Learning Rate**: 0.01
- **Momentum**: 0.9
- **Epochs**: 200
- **Batch Size**: 5
- **Dropout Rate**: 0.5

### Flask Configuration
- **Debug Mode**: Enabled for development
- **Host**: localhost
- **Port**: 5000
- **CORS**: Enabled for cross-origin requests

## 🚀 Deployment

### Local Development
```bash
python app.py
```

### Production Deployment
For production deployment, consider:
- Using a production WSGI server (Gunicorn, uWSGI)
- Setting up environment variables
- Configuring proper logging
- Implementing security measures

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🐛 Troubleshooting

### Common Issues

1. **NLTK Data Not Found**
   ```bash
   python download_nltk_data.py
   ```

2. **TensorFlow Installation Issues**
   ```bash
   pip install tensorflow==2.12.0
   ```

3. **Port Already in Use**
   - Change the port in `app.py` or kill the process using the port

4. **Virtual Environment Issues**
   ```bash
   # Deactivate and recreate
   deactivate
   python -m venv venv
   venv\Scripts\activate  # Windows
   source venv/bin/activate  # macOS/Linux
   ```

## 📞 Support

If you encounter any issues or have questions:
- Check the troubleshooting section above
- Review the code comments for implementation details
- Open an issue on the repository

## 🔮 Future Enhancements

- [ ] Add more conversation topics and intents
- [ ] Implement sentiment analysis
- [ ] Add conversation memory/context
- [ ] Integrate with external APIs
- [ ] Add voice input/output capabilities
- [ ] Implement user authentication
- [ ] Add conversation history
- [ ] Create mobile app interface

---

**Happy Chatting! 🤖💬**
