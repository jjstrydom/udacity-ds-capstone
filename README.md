# Customer Segmentation Report for Arvato Financial Services

For this project demographics data for customers of a mail-order sales company in Germany was analysed. The customer demographics data was compared against demographics information for the general population. Unsupervised learning techniques to perform customer segmentation as well as identifying the parts of the population that best describe the core customer base of the company was performed. A model is trained to predict which individuals are most likely to convert into becoming customers for the company. A third dataset with demographics information for targets of a marketing campaign for the company is used as a validation set. The data used has been provided by Bertelsmann Arvato Analytics.

## Blog post
A blog post outlining this work is published [here](https://medium.com/p/214ddb46c142).

## Environment
This project uses python. The environment is managed using `pipenv`. [This link](https://realpython.com/pipenv-guide/) will help you get started with `pipenv`.

This project uses `python 3.8` and the following packages:
- jupyter = "*"
- numpy = "*"
- pyarrow = "==2.0.0"
- pandas = "*"
- bokeh = "*"
- scipy = "*"
- scikit-learn = "*"
- tqdm = "*"
- xlrd = "*"
- openpyxl = "*"
- umap-learn = "*"
- pandas-bokeh = "*"

For the most up to date information see Pipfile(s) in the root folder.

## Datasets
The general population and customeres datasets is provided as part of the project, and not included in the repository. 
- Path relative to project root folder: `../../data/Term2/capstone/arvato_data/`
- General population filename: `Udacity_AZDIAS_052018.csv`
- Customers filename: `Udacity_CUSTOMERS_052018.csv`
- Mailout validation set: `Udacity_MAILOUT_052018_TRAIN.csv`
- Kaggle submission: `Udacity_MAILOUT_052018_TEST.csv`
In addition to the datasets, as part of the project spreadsheets are provided that describe that dataset. This code utilises the `DIAS Attributes - Values 2017.xlsx` spreadsheet to identify known and unknown columns. This file should be located in the root folder of the project. 

## Files
- `.gitignore`: Specifies directories and files in the project that should not be version controlled and excluded from this repository. 
- `Arvato Project Workbook.ipynb`: The main contribution of this project.
- `Pipfile`: Pipenv file specifying the proejct requirements. 
- `Pipfile.lock`: Pipenv file specifying the installed packages. 
- `LICENSE`: MIT. Read for information on re-use and sharing. Usage of this software, analysis or anything else in this repository is subject to the license.
- `README.md`: This file.

## How to run
1. Activate the environment by running `pipenv shell` in the project folder.
2. Run jupyter using the `jupyter notebook` command. 
3. Open the notebook `Arvato Project Workbook.ipynb` using jupyter.


# Model Performance
A random forest classifier setup with the default hyperparameters produces an AUC of 0.896 on the test set (20% holdout of the training data), and an AUC of 0.799 on the validation set. The kaggle submission ranks this classifier 3rd out of all submissions. 


# Contact
https://github.com/jjstrydom