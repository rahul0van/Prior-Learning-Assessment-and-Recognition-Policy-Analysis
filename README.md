# Prior Learning Assessment and Recognition Policy UCW

## Data Wrangling 

### Project Description
This project focuses on extracting, cleaning, and structuring data of student who are admiting in University Canada West for the "Prior Learning Assessment and Recognition Policy". The objective was to transform the dataset of students to a structured and searchable format suitable for analysis and reporting.

### Project Title
**Data Wrangling for Policy Analysis**

### Objective
To convert dataset into a high-quality, structured dataset for easier interpretation and use. The goal was to ensure accuracy, completeness, and consistency while maintaining the integrity of the original policy content.

### Dataset
The dummy data was  crated from a ChatGPT which include 3 dataset Students Lists, Course List and Credit Granted List which include policy introduction, details, eligibility criteria, and procedures. Key attributes such as section name, student_id, course_id, course_name, credit_granted, and student_gpa  were identified.

---

### Methodology

### **1. Data Ingestion**
- Created an Amazon S3 bucket, “ro-raw-rah,” to store the raw dataset securely.
- Saved the raw data in its original format (Excel) for reprocessing and accessibility.

### **2. Data Profiling**
- Connected the raw dataset in AWS Glue DataBrew for profiling and quality assessment.
- Ran profiling jobs to generate insights about missing values, duplicates, and overall dataset health.
- Identified missing values.
- Saved profiling results in a designated folder within the transformed bucket.


### **3. Data Cleaning**
- Normalized the data by removing extra spaces, line breaks, and special characters.
- Addressed missing values by marking placeholders or filling gaps with additional research.
- Stored cleaned data in two formats: User-readable (CSV) for end user use and Parquet for automated analytics workflows.

---

### Tools and Technologies
- AWS Services: S3, Glue DataBrew
- Data Formats: CSV and Parquet

---

### Deliverables
- A cleaned dataset analysis.
- Outputs in user-readable (CSV) and system-efficient (Parquet) formats.

  <img width="654" alt="image" src="https://github.com/user-attachments/assets/f44ac8a9-3c89-4610-91e7-9d9f2d403480" />

# Data Quality Control 

## Project Description
Data quality control is a crucial step to ensure the dataset's accuracy, completeness, and reliability for analysis. In this project, the quality control process focused on validating the cleaned dataset for completeness, uniqueness, and sensitivity before proceeding to further analysis. The processed data was categorized into **Passed** and **Failed** categories, enabling structured workflows for analysis.

### Project Title
**Data Quality Prior Learning Assessment and Recognition Policy UCW Dataset**

### Objective
To ensure the dataset adheres to predefined quality standards, such as:
1. Completeness of critical attributes.
2. Uniqueness of records to avoid duplication.
3. Identification of sensitive data for compliance and security.

---

## Methodology

### 1. Data Profiling
- Reviewed dataset to identify missing values, duplicates, and inconsistent formatting.

### 2. Data Cleaning
- Handled missing and invalid values during the earlier data cleaning phase.
- Addressed:
  - Special characters in `Name` and `Date`.
  - Inconsistent formats for `Country` and `Date`.

### 3. Data Validation Rules
- **Completeness**:
  - Ensured all rows in `name`, `addresses`, and `cgpa` columns are filled.
- **Uniqueness**:
  - Verified that records are unique based on `student_id`.
- **Sensitive Data Detection**:
  - Checked for potential PII (e.g., addresses, personal identifiers) using AWS Glue's transformation rules.

### 4. Segregation of Data
- **Passed Data**: Records meeting quality criteria stored in the **Passed** folder.
- **Failed Data**: Incomplete or inconsistent records flagged and stored in the **Failed** folder.

### 5. Output
- Cleaned and validated data stored in:
  - **Passed**: `s3://ro-trf-rah/student_admission/data-quality/Passed/`
  - **Failed**: `s3://ro-trf-rah/student_admission/data-quality/Failed/`

---

## Tools and Technologies
- **AWS Glue**: Data quality transformation and sensitive data detection.
- **AWS S3**: Storage for cleaned and validated datasets.
- **File Formats**: Parquet for system use; CSV for end-user accessibility.


  <img width="329" alt="image" src="https://github.com/user-attachments/assets/15990851-1abb-4d8b-9b5f-ca7550c4ce8c" />


---

### Conclusion
This project successfully demonstrated the ability to clean and wrangle dataset. By applying systematic data cleaning and transformation techniques, the project delivered a high-quality dataset that can be leveraged for analysis, reporting, or integration into digital systems. The structured data provides improved accessibility and usability, ensuring better alignment with organizational objectives.
