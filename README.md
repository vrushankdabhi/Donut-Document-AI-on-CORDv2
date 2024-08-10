Here's a sample `README.md` file tailored to your project, using the Donut model and the CORD v2 dataset:

---

# Donut Document AI on CORDv2

## Project Overview

This repository contains the implementation of a Document AI system using the **Donut (Document Understanding Transformer)** model fine-tuned on the **CORD v2 (Consolidated Receipt Dataset)**. The system is designed to automatically extract and process information from receipt documents, converting them into structured data formats such as Excel sheets.

## Model

### Donut (Document Understanding Transformer)
- **Architecture:** End-to-end transformer model designed for document understanding.
- **Capabilities:** Integrates OCR and information extraction into a single process, making it highly efficient for tasks involving complex document layouts like receipts and invoices.
- **Fine-Tuning:** The model was fine-tuned on the CORD v2 dataset to extract key information from receipt documents, including merchant names, dates, item descriptions, prices, and totals.

### Hugging Face Model Link
The fine-tuned model is available on Hugging Face: [Donut Document AI](https://huggingface.co/vrushankkk/donutDocAI).

## Dataset

### CORD v2 (Consolidated Receipt Dataset)
- **Description:** A dataset consisting of annotated receipts from various vendors and formats, specifically designed for OCR and information extraction tasks.
- **Annotations:** Key information such as merchant names, dates, items, prices, and totals is annotated.
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

## Repository Structure

```bash
├── Donut_AI_Python_Script.ipynb  # Jupyter notebook for training and inference
├── examples/
│   ├── input_docs/               # Directory containing example input documents
│   └── output/                   # Directory containing example output files
├── README.md                     # This readme file
└── requirements.txt              # Required dependencies
```

## Conclusion

This project demonstrates the application of the Donut model for document understanding tasks, specifically in the banking and finance sector for processing receipts. The combination of the Donut model and the CORD v2 dataset provides a robust solution for automating the extraction of structured information from complex document layouts.

Feel free to explore, use, and contribute to this repository!

---

This README template covers all the essential aspects of your project and guides users through the process of using your code, understanding the model, and exploring the dataset. Make sure to adjust the content to fit any additional specifics of your project.
