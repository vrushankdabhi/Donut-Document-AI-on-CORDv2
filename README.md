Here's a sample `README.md` file tailored to your project, using the Donut model and the CORD v2 dataset:

---

# Donut Document AI on CORDv2

## Project Overview

This repository contains the implementation of a Document AI system using the **Donut (Document Understanding Transformer)** model fine-tuned on the **CORD v2 (Consolidated Receipt Dataset)**. The system is designed to automatically extract and process information from receipt documents, converting them into structured data formats such as Excel sheets.

## Model

### Donut (Document Understanding Transformer)
Donut, is an end-to-end transformer model designed specifically for processing and extracting structured information from document images. Unlike traditional OCR-based pipelines that require separate stages for text recognition and information extraction, Donut integrates these tasks into a single, unified model, streamlining the workflow and enhancing efficiency.


### End-to-End Architecture:
Efficiency: 
Donut's architecture eliminates the need for separate OCR and information extraction steps by processing document images directly to extract structured information. This end-to-end approach reduces the complexity of the pipeline and minimises potential error propagation between stages.

Suitability for Complex Layouts: 
The model is particularly effective for documents with complex layouts, such as invoices and receipts, where fields like dates, amounts, and item descriptions need to be accurately identified and extracted.

Ease of Fine-Tuning:
Pre-trained on Diverse Document Types- Donut is pre-trained on a variety of document types, making it adaptable to specific tasks with minimal additional training. Fine-tuning Donut on a dataset like "Invoices and Receipts OCR v1" involves adjusting the model to recognize specific fields relevant to financial documents, a process that is well-supported by Donut’s architecture.
Minimal Data Requirement- Fine-tuning Donut requires less annotated data compared to models that need extensive separate datasets for OCR and information extraction. This makes it practical and cost-effective to adapt Donut to specific use cases.

Support for Various Formats:
Versatility- Donut is capable of handling a wide range of document formats, including invoices, receipts, forms, and other structured documents. This versatility ensures that the model can be effectively applied across different types of banking documents, enhancing its utility in real-world applications.
Robust to Noise and Variations- The model is designed to be robust to variations in document quality, such as differences in lighting, resolution, and noise, which are common challenges in processing scanned documents.

Model Architecture: 
Transformer-Based- Donut leverages a transformer architecture, which is known for its ability to capture global context and relationships within the data. This architecture is particularly advantageous for understanding the layout and structure of documents, ensuring that the model can accurately identify and extract relevant information.
Pre-trained on Synthetic and Real-World Data- The model has been trained on a combination of synthetic and real-world document data, allowing it to generalise well to unseen document types and layouts, further enhancing its adaptability and performance.

Conclusion:
Donut is the most suitable pre-trained Document AI model for the task of extracting information from invoices and receipts. Its end-to-end processing capability, ease of fine-tuning, and support for various document formats make it an ideal choice for automating information extraction tasks. The model's architecture ensures high accuracy and robustness, particularly in scenarios involving complex document layouts and noisy data.


### Hugging Face Model Link
The fine-tuned model is available on Hugging Face: [Donut Document AI](https://huggingface.co/vrushankkk/donutDocAI).

## Dataset

### CORD v2 (Consolidated Receipt Dataset)

The CORD v2 dataset, available on Hugging Face, is a robust and comprehensive collection of annotated receipts, making it an ideal choice for training the Donut model for document understanding tasks in the banking sector. This dataset is specifically designed for the extraction of key information from receipts, including various formats and types of fields typically found in financial documents.

- **Dataset Link:** The dataset can be accessed from [Hugging Face Datasets](https://huggingface.co/datasets/naver-clova-ix/cord-v2).

## Python Script

The `Donut_AI_Python_Script.ipynb` notebook contains the code to:

1. **Load and Preprocess Data:** Prepare the CORD v2 dataset for training and evaluation.
2. **Fine-Tune the Model:** Adapt the Donut model to the specific task of receipt information extraction.
3. **Infer and Extract Information:** Use the fine-tuned model to extract structured information from new receipts.
4. **Export Results:** Convert the extracted information into an Excel sheet.

### Usage Instructions

1. **Environment Setup:**
   - Clone the repository:
     ```bash
     git clone https://github.com/vrushankdabhi/Donut-Document-AI-on-CORDv2.git
     cd Donut-Document-AI-on-CORDv2
     ```
   - Install the required dependencies:
     ```bash
     pip install -r requirements.txt
     ```

2. **Run the Notebook:**
   - Open `Donut_AI_Python_Script.ipynb` in Jupyter Notebook or any compatible environment.
   - Follow the steps in the notebook to load the model, preprocess the data, and infer the results.

3. **Input and Output:**
   - Place the PDF receipts you want to process in the `input_docs/` directory.
   - Run the notebook to process the documents.
   - The extracted data will be saved as an Excel sheet in the `output/` directory.

## Examples

### Input
- Sample PDF receipt document: `input_docs/sample_receipt.pdf`

### Output
- Structured data in Excel format: `output/sample_receipt.xlsx`


## Conclusion

This project demonstrates the application of the Donut model for document understanding tasks, specifically in the banking and finance sector for processing receipts. The combination of the Donut model and the CORD v2 dataset provides a robust solution for automating the extraction of structured information from complex document layouts.
