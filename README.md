# Machine Learning Project: Predicting Air Pollution in African Cities
In this project, we aimed to predict PM2.5 concentrations based on 3 months of weather in various cities around the globe. Our team tested & developed 3 models using SVM, Random Forest & Logistic Regression algorythms, achieving a final F1 Beta score of 0.69 (SVM). The project was completed as part of the neuefische Data Science Bootcamp in February 2023.

## Team
- Stephen Kelly
- Christopher Hedemann
- Sarah Wiesner

## Data Source

Our data was sourced from the [Zindi - Urban Air Pollution Challenge](https://zindi.africa/competitions/zindiweekendz-learning-urban-air-pollution-challenge)

## Repository Structure

- `ML_project_EDA.ipynb`: [Jupyter notebook](./ML_project_EDA.ipynb) containing all EDA work, including cleaning, analysis, modelling, and visualization.
- `ML_project_model_training.ipynb`: [Jupyter notebook](./ML_project_model_training.ipynb) containing saved models.
- `presentation.pdf`: [Presentation](./presentation.pdf) given within the neuefische DS bootcamp.
- `requirements.txt`: [Required packages](./requirements.txt) and dependencies.
- `data`: [Directory](./data) containing data files.

## Setup & Usage

- pyenv
- python==3.9.8

This repo contains a [requirements.txt](./requirements.txt) file with a list of all the packages and dependencies you will need.
For installing the virtual environment you can either use the Makefile and run `make setup` or install it manually with the following commands: 

```Bash
pyenv local 3.9.8
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

In order to train the model and store test data in the data folder and the model in models run:

```bash
#activate env
source .venv/bin/activate

python data/train.py  
```

In order to test that predict works on a test set you created run:

```bash
python data/predict.py models/linear_regression_model.sav data/X_test.csv data/y_test.csv
```

## Limitations

Development libraries are part of the production environment, normally these would be separate as the production code should be as slim as possible.
