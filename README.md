# Demo Table Extraction
Initially, balance sheet data from various companies is sourced from publicly available platforms such as Google and Zalo. To ensure diversity in the dataset, the CTGAN model is employed to generate synthetic tabular images that replicate the structure of the original data. Subsequently, this enriched dataset is utilized to train the TATR model, which performs two key tasks: table detection and table structure recognition from the input images.
## 1, Generation Table
Technology: Python, CTGAN

![GenTable](GenTable.png)

## 2, Extraction Table
Technology: Python, TATR

![ExtractionTable](TableExtraction.png)
