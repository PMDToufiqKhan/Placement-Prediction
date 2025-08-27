# Placement Prediction

## Overview
Predicts job placement using HSC and degree percentages with a Perceptron model.

## Files
- **PlaceMntPred.ipynb**: Data prep, training, visualization, and model save.
- **app.py**: Loads model for predictions (example script included).

## Requirements
- Python 3.x
- pandas, numpy, matplotlib, scikit-learn, mlxtend

## Usage
1. Run notebook to train and save `Model.pkl`.
2. Use `app.py` for predictions:
   ```python
   import pickle
   import numpy as np
   model = pickle.load(open('Model.pkl', 'rb'))
   prediction = model.predict(np.array([[75.0, 80.0]]))
   print("Placed" if prediction[0] == 1 else "Not Placed")
   ```
