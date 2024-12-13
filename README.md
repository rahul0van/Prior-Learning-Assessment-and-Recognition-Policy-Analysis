# Prior Learning Assessment and Recognition Policy

## Data Wrangling 

### Project Description
This project focuses on extracting, cleaning, and structuring data from the "Prior Learning Assessment and Recognition Policy" PDF document. The objective was to transform the unstructured policy text into a structured and searchable format suitable for analysis and reporting.

### Project Title
**Data Wrangling for Policy Analysis**

### Objective
To convert unstructured policy text into a high-quality, structured dataset for easier interpretation and use. The goal was to ensure accuracy, completeness, and consistency while maintaining the integrity of the original policy content.

### Dataset
The data was extracted from a PDF document and consisted of multiple sections, including policy introduction, details, eligibility criteria, and procedures. Key attributes such as section titles, subsections, descriptions, and examples were identified and structured.

---

### Methodology

### **1. Data Ingestion**
- Downloaded the PDF document from the official website.
- Extracted text and tables using Python libraries like `PyPDF2` and `pdfplumber`.
- Saved the raw data in its original format (JSON) for reprocessing and accessibility.

### **2. Data Profiling**
- Analyzed the structure and quality of the extracted data to identify missing values, duplicates, and inconsistencies.
- Categorized sections by attributes such as `Section`, `Subsection`, `Details`, `Examples`, and `References`.
- Stored profiling results in a structured format for further review.

### **3. Data Cleaning**
- Normalized the text by removing extra spaces, line breaks, and special characters.
- Standardized the casing for section headers and content.
- Addressed missing values by marking placeholders or filling gaps with additional research.

### **4. Data Transformation**
- Converted the unstructured text into a tabular format with columns:
  - `Section`, `Subsection`, `Details`, `Page`, `Tags`.
- Created metadata fields for quick searchability, such as page numbers and section tags (e.g., `Policy`, `Procedure`).
- Grouped related content for better readability and organization.

### **5. Data Validation**
- Cross-checked the cleaned data with the original document to ensure no information was lost or misrepresented.
- Verified consistency in section labeling and alignment with policy headers.

### **6. Output Preparation**
- Saved the processed data in multiple formats:
  - **CSV**: Tabular data for analysis.
  - **JSON**: Structured data for integration into web applications.
  - **PDF/Word**: Cleaned and enhanced versions of the policy document.

---

### Tools and Technologies
- **Data Extraction**: `PyPDF2`, `pdfplumber`
- **Data Cleaning and Transformation**: Python (`Pandas`, `re`)
- **Storage and Formats**: CSV, JSON, PDF
- **Validation**: Manual review and cross-referencing

---

### Deliverables
- A structured dataset in CSV and JSON formats, ready for analysis.
- A cleaned and enhanced version of the policy document.
- Metadata for quick search and categorization.

---

### Conclusion
This project successfully demonstrated the ability to extract and wrangle unstructured policy data into a usable format. By applying systematic data cleaning and transformation techniques, the project delivered a high-quality dataset that can be leveraged for analysis, reporting, or integration into digital systems. The structured data provides improved accessibility and usability, ensuring better alignment with organizational objectives.
