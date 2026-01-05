# ☁️ Cloud Data Processing & ML Service

This project is a simplified "Cloud Service" dashboard built in a Jupyter Notebook (Google Colab). It allows users to upload large data files, perform automatic data analysis, and run Machine Learning jobs to see how well the system scales when using more "nodes" (processing power).

## What does this code do?

*   **Environment Setup:** It installs and initializes PySpark, which is a powerful tool for processing millions of rows of data quickly.
*   **File Uploading:** It creates a local storage system (`/content/cloud_storage`) where you can upload CSV, JSON, or even PDF files.
*   **Data Cleaning & Stats:** Once a file is uploaded, the service automatically calculates "Descriptive Statistics"—things like the average (mean), missing values, and unique counts for every column.
*   **Automated Machine Learning:** If the data is suitable, it runs four types of ML jobs:
    *   **Linear Regression:** To predict numerical values.
    *   **KMeans Clustering:** To group similar data points together.
    *   **Logistic Regression:** For classification tasks.
    *   **FP-Growth:** To find patterns or associations in text data.
*   **Scalability Benchmarking:** This is the "Cloud" part! The code simulates running these jobs on 1, 2, 4, and 8 nodes. It measures the Speedup and Efficiency to show how much faster the work gets done when you add more resources.

## Folder Structure

When you run the code, it sets up two main folders:
*   `uploads/`: Where your raw data files are stored.
*   `results/`: Where the final reports, performance CSVs, and data statistics are saved.

## How to use it

1.  **Run the cells:** Execute the code in order to start the Spark session.
2.  **Dashboard:** A menu will appear asking if you want to upload a file or view results.
3.  **Upload:** Select a dataset (like a CSV).
4.  **Wait for Processing:** Spark will load the data and start the ML benchmarks automatically.
5.  **Check Results:** Look at the `final_scalability_report.csv` in the results folder to see the performance charts.

## Technologies Used

*   **PySpark:** For big data processing and ML.
*   **Pandas/Matplotlib:** For organizing results and showing tables.
*   **PyPDF2:** To allow the system to read text from PDF files.
*   **Google Colab:** The environment where the "Cloud" storage is simulated.


