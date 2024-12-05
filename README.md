# ETL-AI-PIPELINE

# Malware Project

This project involves the preprocessing and analysis of IoT malware capture data. The dataset includes various scenarios of IoT malware captures, and the preprocessing is done using a Jupyter Notebook.

## Files and Directories

  - `Data Preprocessing.ipynb`: Jupyter Notebook for preprocessing the dataset.
  - `Dataset/`: Contains the dataset for the project.
  - `opt/Malware-Project/BigDataset/IoTScenarios/`: Contains various IoT malware capture scenarios.
  - Each scenario folder (e.g., `CTU-IoT-Malware-Capture-1-1`) contains a `bro` directory with a `conn.log.labeled` file.
  - `decisionTreesZeroDiv1.py`: Python script related to decision trees.
  - `Function source GCloud/`: Contains source code and requirements for Google Cloud functions.
  - `main.py`: Main script for Google Cloud functions.
  - `requirements.txt`: Dependencies for Google Cloud functions.
  - `iot23_combined.csv`: Combined CSV file of the processed dataset.
  - `requirements.txt`: Dependencies for the project.
  - `Screenshots/`: Directory for storing screenshots.

## Usage

1. **Preprocessing the Data**:
   - Open `Data Preprocessing.ipynb` in Jupyter Notebook.
   - Run the cells to preprocess the data and generate the combined CSV file (`iot23_combined.csv`).

2. **Running the Scripts**:
   - Use `decisionTreesZeroDiv1.py` for decision tree-related tasks.
   - Use the scripts in `Function source GCloud/` for Google Cloud functions.

3. **Dependencies**:
   - Install the required dependencies using the `requirements.txt` file:
     ```sh
     pip install -r requirements.txt
     ```

## Google Cloud Services

This project utilizes several Google Cloud Services to manage and process the data:

### Google Cloud Functions

Google Cloud Functions are used to run serverless functions that handle specific tasks such as data processing and triggering events. The `main.py` file in the `Function source GCloud/` directory contains the code for these functions.

### Cloud SQL PostgreSQL

Cloud SQL PostgreSQL is used to store the results of the analysis.

### Cloud Storage

Google Cloud Storage is used to store the processed data files and trigger the function. The dataset files are uploaded to a Cloud Storage bucket, and the processed CSV file (`iot23_combined.csv`) is also stored here for easy access and sharing.

### Workflow

1. **Data Upload**:
   - Data files are uploaded to a Cloud Storage bucket.

2. **Data Processing**:
   - Google Cloud Functions are triggered to process the data files.
   - The processed results are stored in a Cloud SQL PostgreSQL instance.

3. **Data Access**:
   - The processed CSV file is stored in Cloud Storage for easy access.

## Dataset

The dataset contains labeled connection logs from various IoT malware capture scenarios. Each `conn.log.labeled` file includes fields such as timestamp, unique ID, source IP, source port, destination IP, destination port, protocol, service, duration, bytes sent, bytes received, connection state, and labels indicating whether the connection is benign or malicious.

## Thanks to

Stratosphere Laboratory. A labeled dataset with malicious and benign IoT network traffic. January 22th. Agustin Parmisano, Sebastian Garcia, Maria Jose Erquiaga.
https://www.stratosphereips.org/datasets-iot23 for the Dataset and Yue (Dylan) Liang for being a guide to comprehend and complete this project.
