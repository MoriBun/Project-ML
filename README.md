# Final Project - Liver Cirrhosis Stage Prediction
Machine Learning final project: analyzing, preprocessing, and building machine learning models to predict the **liver cirrhosis stage (Stage)** based on the `liver_cirrhosis.csv` dataset (25,000 rows, 19 columns).
## Directory structure
```
Project-ML/
├── Code/
│   ├── Code_Final.ipynb     # Main notebook containing all the code
│   └── data/
│       └── data.zip         # Contains liver_cirrhosis.csv
├── Báo cáo.pdf               # Detailed project report
├── Bản trình bày.pdf          # Presentation slides
└── Tệp_thông_tin.pdf         # Group information & instructions for running the program
```
## Work performed
The `Code_Final.ipynb` notebook is organized into the following main sections:
1. **Data preprocessing**: reading the data, preliminary description & statistics, checking for missing/abnormal values, unit conversion, outlier handling, data normalization.
2. **Data analysis and visualization**: examining the distribution of fields, the relationships between features and the disease stage.
3. **Clustering**: applying K-Means, evaluated with WCSS (Elbow) and Silhouette Score.
4. **Classification**: applying and comparing KNN, MLP, and SVM models on the original data and on the dimensionality-reduced data (PCA/LDA).
5. **Regression**: reformulating the stage-classification problem as a regression task, applying MLP and Linear Regression.
## Team members and task allocation
| Member | Student ID | Tasks |
|---|---|---|
| Nguyễn Huy Hoàng (Team leader) | 22000095 | Data preprocessing, data analysis, KNN model (classification), Random Forest (regression) |
| Tạ Đăng Đức | 22000088 | Data clustering, MLP model (classification), Linear Regression (regression) |
| Đào Mạnh Đức | 22000085 | Dimensionality reduction (PCA - LDA), SVM model (classification) |
## How to run the program
The program is built to run on **Google Colab**.
1. Go to [Google Colab](https://colab.research.google.com/) and upload the `Code/Code_Final.ipynb` file.
2. Upload the `Code/data` directory (containing `data.zip`) to Colab, and note the path (e.g. `/content/data`).
3. In the notebook, locate and edit the zip-file path variable to match the actual location, for example:
   ```python
   local_zip = '/content/data/data.zip'
   extract_to = '/content/'
   ```
4. Run the cells in order:
   - Connect to Google Drive (if you use Drive to store the data).
   - Import the required libraries.
   - Extract `data.zip`.
   - Read the data from `liver_cirrhosis.csv`.
   - Subsequent cells: preprocessing, analysis, training, and displaying the model results.
> If you are not running on Colab, adjust the data paths to match your local environment.
For more detailed information about how the program is organized and run, see [Tệp_thông_tin.pdf](Tệp_thông_tin.pdf).
## Related documents
- [Báo cáo.pdf](Báo%20cáo.pdf): the full detailed project report.
- [Bản trình bày.pdf](Bản%20trình%20bày.pdf): presentation slides.
