# Chicken Disease Classification

This project aims to classify diseases in chickens using a deep learning model. The repository contains all the necessary code, configurations, and instructions to train, evaluate, and deploy the model using CI/CD pipelines.

## Interface




## Project Structure

The project is organized into the following directories and files:

1. ├── .github/workflows/
│ └── .gitkeep # Placeholder for GitHub workflows
2. ├── src/chicken_disease_classification/
│ ├── components/ # Components like data ingestion, model training, etc.
│ ├── utils/ # Utility functions for general use
│ ├── config/ # Configuration management
│ ├── pipeline/ # Pipeline scripts to orchestrate the workflow
│ ├── entity/ # Data structures for configuration management
│ └── constants/ # Constant values used throughout the project
3. ├── config/
│ └── config.yaml # Configuration file for managing paths and URLs
4. ├── dvc.yaml # DVC pipeline stages
5. ├── params.yaml # Parameters for model training and preparation
6. ├── requirements.txt # Python dependencies
7. ├── setup.py # Setup script for the Python package
8. ├── research/
│ └── trials.ipynb # Notebook for experimenting and trials
└── templates/
└── index.html # Basic HTML template for web interface


## Getting Started

### Prerequisites

- Python 3.8+
- Git
- DVC (Data Version Control)
- Virtual environment tool (e.g., `venv`, `conda`)

### Setting Up the Environment
 1. Create and Activate a Conda Environment:
     ```bash
     conda create -n chicken python=3.8 -y
  conda activate chicken
 2. Install Dependencies:
     ```bash
     pip install -r requirements.txt

### Project Initialization
 1. Create Necessary Files and Directories:
   Run template.py to create all necessary directories and files:
            ```bash
            python template.py

 2.Add, Commit, and Push to GitHub:
           ```bash
           git add .
           git commit -m "Initial commit"
           git push origin main

### Developing the Package

1. Editable Installation:
   
To use setup.py as a package in editable mode, include -e . in requirements.txt.

2. Logging Setup:
Logs are stored using:
   
         ```bash
           logging.basicConfig(level=logging.INFO, format='[%(asctime)s]: %(message)s:')
3. Creating cnnClassifier Package:

Logging setup for cnnClassifier:
         ```bash
          logging_str = "[%(asctime)s: %(levelname)s: %(module)s: %(message)s]"

4. Testing the Package:

Create main.py and test the cnnClassifier package:
   
       ```bash
       from cnnClassifier import logger
       logger.info("Welcome to my log")

### Data Ingestion
1. Download and Extract Dataset:

    a. Update config.yaml with the dataset URL.
    b. Implement DataIngestion class in data_ingestion.py.
 
2. Pipeline Stages:

    a. Implement pipeline stages in pipeline/stage_01_data_ingestion.py.

### Model Training and Evaluation

1. Prepare Base Model:

    a. Store necessary parameters in params.yaml.
    b. Implement prepare_base_model.py.
   
2. Training and Evaluation:

   Follow the pipeline structure to implement training and evaluation scripts.
### Deployment
1. CI/CD Pipeline with Azure:

 a. Create a Dockerfile and push the image to Azure Container Registry.
 b. Deploy the web app using Azure Web App Service.

2. DVC Pipeline:

  a. Initialize DVC and run the pipeline stages with dvc repro.
### Additional Notes
 a. Artifact Management: Include artifacts/* in .gitignore to avoid adding generated files to the repository.
 b. App Integration: Flask API is used for training, prediction, and root endpoints.
 c. Azure CI/CD: Detailed steps for setting up continuous deployment using Azure.
### Workflow
 1.Update config.yaml.
 2. Update params.yaml.
 3. Implement pipeline stages in the order: Data Ingestion → Prepare Base Model → Training → Evaluation.
 4. Deploy using DVC and Azure.

### Running the Project
 1. DVC Pipeline:
      ```bash
       dvc init
       dvc repro
 2. Flask App:
      ```bash
       python app.py

### Conclusion
This project provides a comprehensive structure for chicken disease classification using deep learning, with CI/CD integration for deployment. Follow the steps above to clone, develop, and deploy the project.  
