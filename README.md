# Spark-Projects: Electric Vehicle Charging Stations Data Analysis
The data from Boulder County, Colorado in 2019.

## Project Overview

This project involves the analysis of electric vehicle (EV) charging stations data for the year 2019 in Boulder County, Colorado. The data provides insights into the charging behavior of EVs across different times of the day. Using Apache Spark, we perform various data analysis tasks such as data cleaning, statistical analysis, and forecasting.

The dataset used for this analysis is `forecasting_all.csv`. It includes the charging data for various stations over the course of 2019, with detailed information on the amount of electricity charged at different times of the day.

## Getting Started

To get started with this project, follow the instructions below:

### Prerequisites

- **Apache Spark**: Ensure you have Spark installed on your machine. You can follow the official installation guide [here](https://spark.apache.org/docs/latest/).
- **Python**: The project uses Python to interact with Spark, so Python 3.x should be installed on your system.
- **FindSpark**: This is a Python library for locating and starting Spark from Python. Install it using pip:

    ```bash
    pip install findspark
    ```

### Installation

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/DAVIDshenghuei/Spark-Projects.git
    cd Spark-Projects
    ```

2. Install the required Python dependencies (if any):

    ```bash
    pip install -r requirements.txt
    ```

3. Download the dataset `forecasting_all.csv` and place it in the root directory of the project.

### Setting Up a Spark Session

To start the analysis, we first need to initiate a Spark session:

```python
import findspark
findspark.init()

from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("ElectricVehicleCharging").getOrCreate()
