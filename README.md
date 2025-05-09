# SMS Spam Detection with Fine-Tuned Llama 2

## Project Overview
This project implements an end-to-end SMS spam detection system using Llama 2 through Ollama, featuring:
- **Few-shot learning** for spam classification
- **Automated analysis** using LLM-generated insights
- **Professional report generation** with embedded visualizations

## Key Features
- 🚀 **Llama 2 Integration**: Local model execution via Ollama (no API keys required)
- 📊 **Advanced Analytics**: Performance metrics with confusion matrix analysis
- 🤖 **AI-Powered Reporting**: Automated report generation using Llama 2
- 📈 **Visualization Pipeline**: Automatic plot generation for results interpretation

## Dataset
The [SMS Spam Collection Dataset](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset) from UCI contains 5,574 labeled SMS messages (ham/spam).

## Implementation Highlights

### Notebook 2: Llama 2 Classification
```python
# Few-shot learning implementation
response = ollama.generate(
    model='llama2',
    prompt="""Classify as spam/ham: "Win a free iPhone!" 
    Examples: 
    - "Free prize" → spam 
    - "Meeting at 3pm" → ham""",
    options={'temperature': 0}
)