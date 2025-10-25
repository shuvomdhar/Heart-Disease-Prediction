# Heart Disease Prediction System

A machine learning-powered web application built with Streamlit that predicts the risk of heart disease using K-Nearest Neighbors (KNN) algorithm.

## Overview

This application provides an interactive interface for predicting heart disease risk based on various medical and physiological parameters. The KNN model was selected after testing multiple algorithms due to its superior performance with over 85% accuracy.

## Features

- **Interactive Web Interface**: User-friendly Streamlit application for easy data input
- **Real-time Predictions**: Instant heart disease risk assessment
- **High Accuracy**: KNN model achieving >85% accuracy score
- **Comprehensive Input Parameters**: Evaluates multiple cardiovascular risk factors

## Technical Stack

- **Frontend**: Streamlit
- **Machine Learning**: K-Nearest Neighbors (KNN) Algorithm
- **Data Processing**: Pandas, Scikit-learn
- **Model Persistence**: Joblib

## Model Files Required

The application requires three pre-trained model files:

1. `KNN_heart.pkl` - Trained KNN model
2. `scaler.pkl` - Feature scaler for data normalization
3. `columns.pkl` - Expected feature columns for consistent input

## Input Parameters

The application collects the following patient information:

| Parameter | Type | Range/Options | Description |
|-----------|------|---------------|-------------|
| Age | Slider | 18-100 years | Patient's age |
| Sex | Dropdown | M/F | Patient's biological sex |
| Chest Pain Type | Dropdown | ATA, NAP, TA, ASY | Type of chest pain experienced |
| Resting BP | Number | 80-200 mm Hg | Resting blood pressure |
| Cholesterol | Number | 100-600 mg/dl | Serum cholesterol level |
| Fasting BS | Dropdown | 0/1 | Fasting blood sugar > 120 mg/dl |
| Resting ECG | Dropdown | Normal, ST, LVH | Resting electrocardiogram results |
| Max HR | Slider | 60-220 bpm | Maximum heart rate achieved |
| Exercise Angina | Dropdown | Y/N | Exercise-induced angina |
| Oldpeak | Slider | 0.0-6.0 | ST depression induced by exercise |
| ST Slope | Dropdown | UP, Flat, Down | Slope of peak exercise ST segment |

### Parameter Definitions

- **ATA**: Atypical Angina
- **NAP**: Non-Anginal Pain
- **TA**: Typical Angina
- **ASY**: Asymptomatic
- **LVH**: Left Ventricular Hypertrophy
- **ST**: ST-T Wave Abnormality
- **Oldpeak**: ST depression relative to rest

## Installation

1. Clone the repository:
```bash
git clone https://github.com/shuvomdhar/Heart-Disease-Prediction.git
cd Heart-Disease-Prediction
```

2. Install required dependencies:
```bash
pip install streamlit pandas joblib sklearn
```

3. Ensure model files are in the project directory:
   - KNN_heart.pkl
   - scaler.pkl
   - columns.pkl

## Usage

1. Run the Streamlit application:
```bash
streamlit run app.py
```

2. Open your browser and navigate to the provided local URL (typically `http://localhost:8501`)

3. Input patient information using the interactive form

4. Click the "Predict" button to receive risk assessment

## Output

The application provides two possible outcomes:

- **⚠️ High Risk of Heart Disease**: Indicates elevated risk requiring medical attention
- **✅ Low Risk of Heart Disease**: Indicates lower probability of heart disease

## Model Performance

The KNN algorithm was selected after comprehensive testing of multiple machine learning algorithms:

- **Accuracy**: >85%
- **Algorithm**: K-Nearest Neighbors (KNN)
- **Feature Engineering**: One-hot encoding for categorical variables
- **Preprocessing**: StandardScaler normalization

## How It Works

1. **Data Collection**: User inputs are collected through Streamlit widgets
2. **Feature Engineering**: Categorical variables are one-hot encoded to match training format
3. **Normalization**: Input features are scaled using the pre-trained scaler
4. **Prediction**: KNN model predicts risk based on normalized features
5. **Result Display**: Risk assessment is presented with visual indicators

## Important Notes

⚠️ **Medical Disclaimer**: This application is for educational and informational purposes only. It should not be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult with qualified healthcare providers for medical decisions.

## Future Enhancements

- Model performance metrics dashboard
- Patient history tracking
- Export prediction reports
- Multiple model comparison
- Confidence score display
- Risk factor visualization

## Requirements

```
streamlit
pandas
joblib
scikit-learn
```

## License

This project is open-source and available for educational use. Feel free to modify and distribute according to your needs.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

---

**Note**: Ensure all model files are properly trained and validated before deployment. Regular model retraining with updated data is recommended to maintain prediction accuracy.