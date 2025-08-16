# Resume Classification System

An intelligent machine learning system that automatically classifies resumes into predefined job categories using Natural Language Processing (NLP) techniques and supervised classification algorithms.

## 🎯 Overview

This project implements an automated resume classification system that analyzes resume content and categorizes them into appropriate job roles such as Software Developer, Data Scientist, Web Developer, and more. The system leverages advanced NLP techniques and machine learning algorithms to achieve high accuracy in classification tasks.

The project is designed to assist:
- **Recruiters** in automatically sorting and categorizing large volumes of resumes
- **Job seekers** in understanding how their resumes align with specific job categories
- **HR departments** in streamlining the initial screening process

## ✨ Features

- **Automated Text Preprocessing**: Comprehensive text cleaning, normalization, and feature extraction
- **Multiple Vectorization Techniques**: TF-IDF, Count Vectorization, and N-gram analysis
- **Advanced Feature Engineering**: Handcrafted features combined with text-based features
- **Model Comparison**: Systematic evaluation of multiple ML algorithms
- **Hyperparameter Optimization**: Grid search with cross-validation for optimal performance
- **Detailed Analytics**: Feature importance analysis and model interpretability
- **Scalable Pipeline**: Modular design for easy extension and modification

## 📊 Dataset

The project uses the [Resume Dataset from Kaggle](https://www.kaggle.com/datasets/gauravduttakiit/resume-dataset) containing:
- **962 resume samples** across multiple job categories
- **Text-based resume content** with varying formats and lengths
- **Job category labels** for supervised learning

### Dataset Statistics
- Total Records: 962
- Feature Dimensions: 5,010 (after feature engineering)
- Training Samples: 769
- Test Samples: 193
- Matrix Sparsity: 96.28%

## 🚀 Installation

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook


## 📁 Project Structure

resume-classification/
│
├── data/
│ ├── raw/ # Original dataset
│ ├── processed/ # Preprocessed data
│ └── preprocessed_resume_dataset.csv
│
├── models/
│ ├── best_model_logistic_regression.pkl
│ ├── label_encoder.pkl
│ ├── tfidf_vectorizer.pkl
│ └── feature_scaler.pkl
│
├── notebooks/
│ ├── 01_data_exploration.ipynb
│ ├── 02_preprocessing.ipynb
│ ├── 03_feature_engineering.ipynb
│ └── 04_model_training.ipynb
│
├── src/
│ ├── preprocessing.py # Text preprocessing functions
│ ├── feature_engineering.py # Feature extraction utilities
│ ├── model_training.py # Model training pipeline
│ └── utils.py # Helper functions
│
├── results/
│ ├── model_comparison_results.csv
│ ├── training_metadata.pkl
│ └── confusion_matrix.png
│
├── requirements.txt
├── README.md
└── LICENSE


## 🔬 Methodology

### 1. Data Preprocessing
- **Text Cleaning**: Removal of emails, phone numbers, URLs, and special characters
- **Normalization**: Lowercasing, whitespace standardization
- **Stopword Removal**: Elimination of common words and domain-specific stopwords
- **Lemmatization**: Reduction of words to root forms

### 2. Feature Engineering
- **TF-IDF Vectorization**: Term frequency-inverse document frequency weighting
- **N-gram Analysis**: Unigram and bigram feature extraction
- **Handcrafted Features**: Resume-specific features (education mentions, technical skills, etc.)
- **Dimensionality Reduction**: SVD for computational efficiency
- **Feature Selection**: Chi-square test for identifying discriminative features

### 3. Model Selection
- **Algorithms Evaluated**: Naive Bayes, Logistic Regression, Random Forest, SVM, Gradient Boosting, KNN
- **Hyperparameter Tuning**: Grid search with stratified cross-validation
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score
- **Model Comparison**: Systematic performance analysis across different feature combinations

## 📈 Results

### Best Model Performance
- **Algorithm**: Logistic Regression (tuned)
- **Test Accuracy**: 85.5%
- **Weighted F1-Score**: 84.7%
- **Cross-Validation Score**: 83.2% ± 2.1%

### Feature Engineering Impact
- **Original Vocabulary**: 5,000 TF-IDF features
- **Selected Features**: 30 most discriminative features
- **Additional Features**: 10 handcrafted resume-specific features
- **Final Feature Matrix**: 5,010 dimensions with 96.28% sparsity

### Top Discriminative Features
1. advocate
2. art
3. blockchain
4. cisco
5. civil
6. civil engineer
7. court
8. data science
9. dot
10. dot net

## 🎯 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score | Training Time |
|-------|----------|-----------|--------|----------|---------------|
| Logistic Regression (Tuned) | 0.8550 | 0.8521 | 0.8550 | 0.8471 | 2.34s |
| Random Forest (Tuned) | 0.8238 | 0.8195 | 0.8238 | 0.8156 | 15.67s |
| Naive Bayes | 0.8031 | 0.7986 | 0.8031 | 0.7923 | 0.12s |
| SVM Linear | 0.7927 | 0.7884 | 0.7927 | 0.7845 | 8.91s |

## 🛠 Technologies Used

- **Programming Language**: Python 3.8+
- **Machine Learning**: scikit-learn
- **Natural Language Processing**: NLTK
- **Data Manipulation**: pandas, NumPy
- **Visualization**: matplotlib, seaborn, wordcloud
- **Development Environment**: Jupyter Notebook
- **Model Serialization**: pickle, joblib

## 🚀 Future Enhancements

### Planned Improvements
- [ ] **Deep Learning Integration**: Implement BERT/Transformer-based models
- [ ] **Web Application**: Deploy as a Flask/Django web service
- [ ] **API Development**: REST API for integration with external systems
- [ ] **Real-time Processing**: Streaming classification for high-volume scenarios
- [ ] **Multi-language Support**: Extend to non-English resumes
- [ ] **Advanced Analytics**: Skill gap analysis and job matching recommendations

### Technical Enhancements
- [ ] **Model Ensemble**: Combine multiple models for improved accuracy
- [ ] **Active Learning**: Incorporate feedback loop for continuous improvement
- [ ] **Explainable AI**: Enhanced model interpretability features
- [ ] **Automated Retraining**: Pipeline for model updates with new data

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Setup
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines
- Follow PEP 8 style guidelines
- Add unit tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting


## 🙏 Acknowledgments

- [Kaggle Resume Dataset](https://www.kaggle.com/datasets/gauravduttakiit/resume-dataset) for providing the training data
- scikit-learn community for excellent machine learning tools
- NLTK team for comprehensive natural language processing capabilities

---

⭐ **Star this repository if you found it helpful!**

*Last updated: August 17, 2025*
