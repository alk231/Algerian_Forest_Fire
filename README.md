# Algerian Forest Fire Prediction 🌲🔥

A machine learning project that predicts the Fire Weather Index (FWI) based on various meteorological factors. This helps in estimating the risk of forest fires in the Algerian region.

## 🧐 What's This Project?

This is an end-to-end machine learning application I built to understand how weather conditions affect forest fire risks. It uses the **Algerian Forest Fires Dataset** to train a Ridge Regression model, which is then served through a Flask web application.

The idea is simple: you enter weather details like temperature, humidity, and wind speed, and the model tells you the predicted fire risk score.

## 🛠️ Tech Stack

- **Python**: Core language
- **Flask**: For the web server and API
- **Scikit-learn**: For model training (Ridge Regression) and preprocessing
- **Pandas & NumPy**: For data manipulation
- **AWS Elastic Beanstalk**: Configuration included for deployment

## 📂 Project Structure

```
Algerian_Forest_Fire/
├── application.py       # Main Flask application
├── requirements.txt     # Dependencies
├── .ebextensions/       # AWS Elastic Beanstalk config
├── dataset/             # Raw dataset
├── models/              # Saved pickle files (model & scaler)
├── notebook/            # Jupyter notebook for EDA and training
└── templates/           # HTML files for the web interface
```

## 📊 The Dataset

The dataset contains data from two regions in Algeria:
- **Bejaia Region** (humid)
- **Sidi Bel-Abbes Region** (semi-arid)

It includes features like:
- **Temperature**: Max temperature in Celsius
- **RH**: Relative Humidity %
- **Ws**: Wind speed in km/h
- **Rain**: Total day in mm
- **FFMC**: Fine Fuel Moisture Code
- **DMC**: Duff Moisture Code
- **ISI**: Initial Spread Index
- **Classes**: Fire or No Fire (encoded)
- **Region**: 0 for Bejaia, 1 for Sidi Bel-Abbes

## 🚀 How to Run locally

1. **Clone the repo**
   ```bash
   git clone https://github.com/alk231/Algerian_Forest_Fire.git
   cd Algerian_Forest_Fire
   ```

2. **Create a virtual environment (Optional but recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the app**
   ```bash
   python application.py
   ```

5. **Open in browser**
   Go to `http://127.0.0.1:5000` to see the interface.

## 🧠 Model Details

I used **Ridge Regression** for this project because it handles multicollinearity well (which is common in weather data).
- The data was standardized using `StandardScaler`.
- The model and scaler are saved in the `models/` directory as `.pkl` files.

## ☁️ Deployment

The project includes an `.ebextensions` folder, making it ready for deployment on **AWS Elastic Beanstalk**. You can deploy it directly by creating an environment in AWS EB.

## 🤝 Contributing

Feel free to fork this, play around with the notebook, or try different models! Open a PR if you have any cool improvements.

## 👤 Author

**Alok Kumar**
- GitHub: [@alk231](https://github.com/alk231)

---
*Built while exploring regression techniques and Flask deployment.*
