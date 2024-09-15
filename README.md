# 🏢 Business Licensing Data Analysis for Vancouver City Office

As a data analyst for the Vancouver City Office, I undertook a comprehensive project to analyze and optimize the business licensing process for companies in Vancouver. Utilizing datasets for 2023 and 2024 sourced from [OpenData Vancouver](https://opendata.vancouver.ca/explore/dataset/business-licences/export/?disjunctive.status&disjunctive.businesssubtype&refine.businesstype=Information+Communication+Technology), I developed a Data Analytics Platform (DAP) to drive insightful metrics and streamline operations.

**Project Overview**
The primary goal of this project was to:
- Analyze and optimize the business licensing process in Vancouver.
- Implement a DAP encompassing descriptive, diagnostic, predictive, and prescriptive metrics to provide valuable insights for decision-making.

**Key Steps in the Project**
1. Data Acquisition and Initial Design:
- Downloaded business license datasets (2023 and 2024) from the operational data source.
- Designed the DAP architecture, defining descriptive, diagnostic, predictive, and prescriptive metrics.
- Created a structured storage design to facilitate data management.
2. Data Storage Design:
- Developed a comprehensive storage solution using AWS S3 to securely store raw data and facilitate easy access for processing.
- Defined general server contents and data analytic platform architecture, establishing a foundation for data transformation and analysis.
3. Data Cleaning and Transformation:
- Utilized AWS Glue DataBrew to clean and preprocess the original Excel dataset, ensuring data quality and consistency.
- Detected and managed sensitive data, evaluated data quality, and applied a conditional router to ensure only high-quality data proceeded through the pipeline.
4. Trusted Zone Creation and Curation:
- Created a Trusted Zone using AWS Glue's components:
  - Sensitive Data Detection: Identified and managed sensitive information.
  - Data Quality Evaluation: Assessed the quality of incoming data.
  - Conditional Routing: Ensured that only validated data was processed.
  - Applied aggregation and join components to create a Curated Zone for advanced analytics.
5. Data Pipeline Design and Implementation:
- Built an end-to-end data pipeline in AWS Glue for seamless data ingestion, transformation, and storage.
- Implemented the ETL process to automate the extraction, transformation, and loading of data into structured formats ready for analysis.
6. Data Analysis and Publishing:
- Leveraged AWS EC2 and AWS Athena to analyze the curated data and derive actionable insights.
- Developed comprehensive visualizations and reports to present the analysis results, providing a clear overview of business licensing trends and optimization opportunities.

**Visual Representations**

The following screenshots capture key aspects of the project:
- **DAP Design:** Outlines the descriptive, diagnostic, predictive, and prescriptive metrics framework.
- **Data Storage Design:** Illustrates the data storage architecture and structure.
- **ETL Implementation:** Depicts the detailed ETL process for transforming and loading data.
- **Trusted Data Pipeline Design:** Presents the creation of a trusted data pipeline using AWS Glue components.

## 🗄️ DAP Design and Data Storage Design
Objective: Design a scalable and secure storage solution for operational data.

The storage design ensures that all raw data is efficiently stored in **AWS S3 Buckets**, allowing for scalability and secure access. This design supports the ingestion of various operational data from different sources, with proper organization to facilitate further processing.

<img width="753" alt="Data Storage Design 2" src="https://github.com/user-attachments/assets/d1e2ab79-cf1a-4761-8c2b-9638849f174b">

The DAP design focuses on:
- Descriptive Metric: Application issued rate to assess current status.
- Diagnostic Metric: Inactive application submission rate to identify underlying issues.
- Predictive Metric: Forecasting future application submissions.
- Prescriptive Metric: Optimal licensing strategy index to provide actionable insights.

## 🔧 ETL Implementation
Objective: Automate the extraction, transformation, and loading of operational data for analysis.

The **ETL (Extract, Transform, Load)** implementation is responsible for automating the data pipeline from raw ingestion to transformation. It includes processes such as filtering, grouping, and applying transformations before storing the final data in structured formats.

AWS Glue ETL Workflow Design is shown below
<img width="1280" alt="ETL Implementation" src="https://github.com/user-attachments/assets/edd5f39f-4817-4dd6-af28-eec7a59715ba">


## 🔄 Trusted Data Pipeline Components
Objective: Implement a pipeline that can handle data ingestion, transformation, quality checks, and routing based on predefined rules.

The data pipeline is composed of several critical components:
- **Data Loading**: Raw data is loaded from **S3 Buckets**.
- **Sensitive Data Detection**: Ensures any PII or sensitive information is identified.
- **Data Quality Evaluation**: Analyzes the quality of data to meet business standards.
- **Conditional Routing**: Based on data analysis, the pipeline can route data to different paths.
- **Transformation**: Final data is transformed and stored in the correct schema for further use.

The design below shows the creation of a trusted data pipeline using AWS Glue, including the stages for detecting sensitive data, evaluating data quality, and routing data conditionally.
<img width="715" alt="Screenshot 2024-09-09 at 2 52 50 PM" src="https://github.com/user-attachments/assets/153a788f-86f4-454e-a29c-ed66a8db9c2d">



