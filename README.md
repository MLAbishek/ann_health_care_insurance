# ann_health_care_insurance

This project implements a machine learning model to predict insurance-related outcomes based on various customer attributes. The model uses a neural network implemented with TensorFlow and preprocesses data using scikit-learn.

## Project Overview

The main components of this project are:
1. Data loading and preprocessing
2. Model loading (pre-trained neural network)
3. Feature encoding and scaling
4. Prediction generation
5. Results output to CSV

## Dependencies

This project requires the following Python libraries:
- pandas
- numpy
- tensorflow
- joblib
- scikit-learn (implicit dependency for preprocessing)

You can install these dependencies using pip:

```
pip install pandas numpy tensorflow joblib scikit-learn
```

## File Structure

- `main.py`: The main script that loads data, preprocesses it, generates predictions, and saves results.
- `/kaggle/input/test-insurance-abi/test_insurance.csv`: Input data file
- `/kaggle/input/test-insurance-abi-v2/kaggle/best_model.keras`: Pre-trained neural network model
- `/kaggle/input/test-insurance-abi-v2/kaggle/lr_encoder.pkl`: Preprocessor for categorical variables
- `/kaggle/input/test-insurance-abi-v2/kaggle/sc_scaler.pkl`: Scaler for numerical variables

## Usage

1. Ensure all dependencies are installed and the required input files are in the correct locations.
2. Run the main script:

```
python main.py
```

3. The script will generate predictions and save them in a file named `answer.csv` in the current directory.

## Input Data Format

The input data should be a CSV file with the following columns:
- id
- Gender
- Age
- Driving_License
- Region_Code
- Previously_Insured
- Vehicle_Age
- Vehicle_Damage
- Annual_Premium
- Policy_Sales_Channel
- Vintage

## Output

The script generates a CSV file named `answer.csv` with two columns:
- id: The customer ID from the input data
- Response: The predicted probability (between 0 and 1)

## Note

This model assumes that the preprocessing steps (encoding and scaling) match those used during the model's training phase. Ensure that any changes to the preprocessing pipeline are consistent with the model's expectations.

## License

MIT License

Copyright (c) 2024 J.Abishek

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
