# AWS Designs

I created the following designs as Cloud Computing Design

## 🗄️ Data Storage Design
Objective: Design a scalable and secure storage solution for operational data.

The storage design ensures that all raw data is efficiently stored in **AWS S3 Buckets**, allowing for scalability and secure access. This design supports the ingestion of various operational data from different sources, with proper organization to facilitate further processing.

<img width="753" alt="Data Storage Design 2" src="https://github.com/user-attachments/assets/d1e2ab79-cf1a-4761-8c2b-9638849f174b"># AWS_Design

## 🔧 ETL Implementation
Objective: Automate the extraction, transformation, and loading of operational data for analysis.

The **ETL (Extract, Transform, Load)** implementation is responsible for automating the data pipeline from raw ingestion to transformation. It includes processes such as filtering, grouping, and applying transformations before storing the final data in structured formats.
<img width="1280" alt="ETL Implementation" src="https://github.com/user-attachments/assets/edd5f39f-4817-4dd6-af28-eec7a59715ba">


## 🔄 Pipeline Components
Objective: Implement a pipeline that can handle data ingestion, transformation, quality checks, and routing based on predefined rules.

The data pipeline is composed of several critical components:
- **Data Loading**: Raw data is loaded from **S3 Buckets**.
- **Sensitive Data Detection**: Ensures any PII or sensitive information is identified.
- **Data Quality Evaluation**: Analyzes the quality of data to meet business standards.
- **Conditional Routing**: Based on data analysis, the pipeline can route data to different paths.
- **Transformation**: Final data is transformed and stored in the correct schema for further use.

<img width="715" alt="Screenshot 2024-09-09 at 2 52 50 PM" src="https://github.com/user-attachments/assets/153a788f-86f4-454e-a29c-ed66a8db9c2d">



