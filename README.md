# survey_contactList

# Introduction

In my previous project (Provider Appointment Availability), we calculate the difference between survey date, and urgent and non-urgent appointments for health care providers contracted with Kentucky Medicaid.

The survey was conducted by vendor via telephone between February 15 to March 24, 2022. The survey was conducted to collect the first available urgent and non-urgent appointment date and time.

- [Click here](https://colab.research.google.com/drive/16jN5pbvAwbe141f1FOvTwKW3stZ4gpF2?usp=sharing) to view my previous project. (Right click to open in new tab) to gain viewer access to the Colab Notebook.

# Methodology

The scope of this project is to generate a Contact List (CL) for vendor, to conduct the telephone survey. The vendor will use the CL to contact providers' office and collect providers appointment date and time availability for Measurement Year (MY) 2023.

Please note, the raw data used in this project is downloaded from Center of Medicare and Medicaid's (CMS) website.[1]

Source:
[1] https://data.cms.gov/provider-data/dataset/mj5m-pzi6

This program will analyze the data downloaded from CMS website and generate the Contact List.

Analyze data:
* Import data downloaded from CMS website into the program.
* Select only required columns to identify providers, such as NPI, First_Name, Last_Name, Type_of_Licensure, Address, City, State, Zip_Code, and Phone_Number, etc.
* Clean data, such as Phone_number, and remove any null or invalid phone numbers.
* Select providers from Kentucky only for CL.
* Sample data using Python function to select random sample.
* Bump sampled data against Provider Appointment Availability survey data to check if the selected providers were contacted in last survey.

Display analyzed data in charts:
* Display sampled data using charts.
* By provider type/ by county

# Project Folder Contents:
	- **README.md**: About the project
	- **LICENSE**: License Document
	- **provider_directory.ipynb**: Program File
	- **DACNationalProvider.csv**: Data File
	- **requirements.txt**: Required libraries to run the program
	- **provider_appt-final.csv**: Output file from Provider Appointment Availability Program

# How to run this program?

## Option 1 - Run using Google Colab. (Easy Method)

If you have a Google account, you can run this code without downloading any programming languages, libraries or tools.

- [Click here](https://colab.research.google.com/drive/16jN5pbvAwbe141f1FOvTwKW3stZ4gpF2?usp=sharing) (Right click to open in new tab) to gain viewer access to the Colab Notebook.
- You may be asked to sign in to your Google account, if you haven't done so already.
- Once the program is open.
    - Click Runtime tab.
    - Click Run All. (Program may auto-run when opened with Google Colab.)
    
## Option 2 - Cloning the repo.

**Running the Program in Jupyter Notebook**
- Clone the repository (git clone https://github.com/shahbijay/survey_contactList).
- Open the clonned repo (project folder) using Jupyter notebook.
- Open **provider_directory.ipynb**
- Click **Cell** tab and then **Run All**.

**Running the Program in PyCharm or other IDE that support Python**
- Clone the repository (git clone https://github.com/shahbijay/survey_contactList).
- Navigate to the saved location of the repo.
- Open the clonned repo (project folder) using PyCharm or any IDE that supports Python, such as ATOM, VS Code, Sublime Text 3, etc.
- Open **provider_directory.ipynb**
- Run program step by step.
- If you are missing any packages or modules, run **pip install -r requirements.txt** to install missing packages or modules.

**Instructions on Installing Anaconda or PyCharm**
- This repo runs on utilizing numbers of libraries that are included with Anaconda. If you do not have Anaconda already installed on your PC, please do so visiting this [link](https://docs.anaconda.com/anaconda/install/index.html) for documentaion on how to install Anaconda.
- This repo runs on latest release of Anaconda. Follow this [instruction](https://docs.anaconda.com/anaconda/install/update-version/) to update Anaconda to latest version.

- Click [here](https://www.jetbrains.com/help/pycharm/installing-uninstalling-and-upgrading-packages.html) for instruction on how to install PyCharm.

If you do not wish to install **Anaconda** or **PyCharm** on your machine and want to run this project locally on your machine or on a virtual environment, please install the requirements.txt by running this command: **pip install -r requirements.txt** in the project folder location or the virtaul environment. This will install necessary libraries to run this program.
