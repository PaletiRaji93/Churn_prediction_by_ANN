# Churn Prediction with Artificial Neural Network

This project is a simple machine learning app for predicting whether a bank customer is likely to churn. The model uses an Artificial Neural Network (ANN) trained on the famous Churn Modelling dataset and is deployed with Streamlit so anyone can try it without writing code.

The goal is straightforward: take customer details like age, balance, credit score, geography, and membership status, and estimate the probability that the customer will leave the bank.

## What this project includes

- ANN-based churn prediction model
- Streamlit web app for real-time prediction
- Data preprocessing with scaling and encoding
- Trained model and saved preprocessing objects
- Notebook experiments for model tuning and testing

## Project structure

- `app.py` -Streamlit app for user input and prediction
- `model.h5`- trained ANN model
- `scaler.pkl` - saved StandardScaler used for feature scaling
- `label_encoder_gender.pkl` -saved gender label encoder
- `onehot_encoder_geo.pkl` - saved geography one-hot encoder
- `Churn_Modelling.csv`-dataset used for training
- `experiments.ipynb`-exploratory model work
- `hyperparametertuningann.ipynb` - tuning experiments
- `prediction.ipynb`-prediction workflow examples
- `requirements.txt`-project dependencies

## Tech stack

- Python
- TensorFlow / Keras
- scikit-learn
- Pandas
- NumPy
- Streamlit

## How the model works

The project uses a customer churn dataset with features such as:

- Credit Score
- Geography
- Gender
- Age
- Tenure
- Balance
- Number of Products
- Has Credit Card
- Is Active Member
- Estimated Salary

These inputs are transformed into the format expected by the neural network, scaled, and passed into the trained ANN model. The output is a probability score between 0 and 1, which can be interpreted as the likelihood of churn.

## Setup

1. Open a terminal in the project folder.
2. Create a virtual environment (optional but recommended):

```bash
python -m venv annvenv
```

3. Activate the environment:

On Windows:

```bash
annvenv\Scripts\activate
```

On macOS/Linux:

```bash
source annvenv/bin/activate
```

4. Install dependencies:

```bash
pip install -r requirements.txt
```

## Run the app

From the project folder, run:

```bash
streamlit run app.py
```

This will launch the web app in your browser. You can then enter customer details and get the churn prediction result instantly.

## Example prediction

The app takes inputs like:

- Geography
- Gender
- Age
- Balance
- Credit score
- Estimated salary
- Tenure
- Number of products
- Credit card status
- Active member status

Then it predicts whether the customer is likely to churn or remain with the bank.

## Notes

This is a beginner-friendly ANN project that shows how a neural network can be used for a real-world classification problem. It is a good example of combining preprocessing, model training, and deployment in a simple end-to-end workflow.

## License

This project is available under the MIT License. See the `LICENSE` file for more details.

## Conclusion

This project demonstrates how machine learning can be used in banking and customer analytics. It is small, practical, and easy to extend with more features, hyperparameter tuning, or a better deployment setup.
