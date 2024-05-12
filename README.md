## MLOps Implementation with Apache Airflow

### Objective
The objective of this project is to implement Apache Airflow to automate the processes of data extraction, transformation, and version-controlled storage. The project utilizes data from dawn.com and BBC.com as data sources, preprocesses the extracted text data, stores the processed data on Google Drive, and implements Data Version Control (DVC) to track versions of the data. Additionally, an Apache Airflow DAG is developed to automate these processes, handling task dependencies and error management effectively.

### Docker Setup
The project is containerized using Docker. Below are the steps to set up Docker:

1. Write a Dockerfile to define the Docker image.
2. Write a docker-compose.yml file to define services, networks, and volumes.
3. Build the Docker image using the Dockerfile.
4. Run the Docker container using docker-compose up command.

### Tasks

#### 1. Data Extraction
   - Utilize dawn.com and BBC.com as data sources.
   - Extract links on the landing page.
   - Extract the titles and descriptions from articles displayed on their homepages.

#### 2. Data Transformation
   - Preprocess the extracted text data by lowercasing the letters and removing unnecessary special characters.

#### 3. Data Storage and Version Control
   - Store the processed data on Google Drive.
   - Implement Data Version Control (DVC) to track versions of the data, ensuring each version is accurately recorded as changes are made.
   - Version the metadata against each DVC push to the GitHub repo.

#### 4. Apache Airflow DAG Development
   - Write an Airflow DAG to automate the processes of extraction, transformation, and storage.
   - Ensure the DAG handles task dependencies and error management effectively.

### Challenges
One of the challenges faced in this project was the difficulty in installing Airflow on Windows and accessing the DAG interface. This challenge was overcome by containerizing the project using Docker, which provided a consistent environment across different operating systems and simplified the deployment process.

### Repository Structure
The repository structure should include the following files and directories:

1. **Dockerfile**: Contains instructions to build the Docker image.
2. **docker-compose.yml**: Defines services, networks, and volumes for Docker.
3. **requirements.txt**: Lists the dependencies required for the project.
4. **README.md**: Provides an overview of the project, setup instructions, and other relevant information.
5. **airflow/**: Directory containing Apache Airflow configuration files.
6. **dags/**: Directory containing Apache Airflow DAG definitions.
7. **scripts/**: Directory containing Python scripts for data extraction, transformation, and other tasks.
8. **data/**: Directory for storing extracted and processed data.
9. **.gitignore**: Specifies intentionally untracked files to ignore.
10. **.dvc/**: Directory containing DVC configuration files.

### Instructions to Run
1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Build the Docker image using the Dockerfile.
4. Run the Docker container using docker-compose up command.
5. Access the Apache Airflow DAG interface in your web browser.

### Conclusion
MLOps implementation with Apache Airflow provides an efficient and automated workflow for managing data extraction, transformation, and version-controlled storage. By containerizing the project with Docker and leveraging Airflow's DAG scheduling capabilities, the project ensures reproducibility, scalability, and maintainability of the data pipeline.