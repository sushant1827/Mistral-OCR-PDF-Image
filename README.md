# 🧠 Mistral OCR with n8n

This n8n workflow automates the extraction of structured information from PDFs and image files using the [Mistral OCR API](https://mistral.ai/). It’s designed for use cases like extracting invoice details or restaurant receipts, and storing them into Google Sheets.

---

## 🔧 Features

- 📄 Upload **PDF invoices** through an n8n form
- 🖼️ Provide **image URLs** (e.g., receipts) for OCR
- 🔍 Uses **Mistral OCR** for high-quality document text extraction
- 🧠 Extracts specific fields using LangChain Information Extractor:
  - For PDFs: 
    - `Invoice Number`
    - `Date`
    - `Gross Amount`
    - `Customer ID`
  - For images:
    - `Restaurant Name`
    - `Date`
    - `Total Bill Amount`
- 📤 Appends extracted data to a **Google Sheets document**
- 💬 Integrated OpenAI Chat node (optional) for further enrichment or validation

---

## 🧩 Workflow Nodes Overview

- **Form Trigger** – Collects PDF invoices from users
- **Set Node** – Allows testing with static image URLs
- **Mistral API Integration** – Handles:
  - File upload
  - Signed URL generation
  - OCR processing
- **LangChain Extractors** – Converts OCR'd text into structured fields
- **Google Sheets Node** – Writes the extracted information to a live spreadsheet
- **OpenAI Chat Node** – Optionally reviews or interprets the data

---

## 🧩 PDF Workflow

![image](https://github.com/user-attachments/assets/b2248052-9937-4fc8-aaa1-5deda174e200)

---

## 🧩 Image Workflow

![image](https://github.com/user-attachments/assets/d34bb967-2318-41dd-9f9c-d0373b62bccb)

---

## 🛠 Requirements

- n8n setup (local or cloud)
- Mistral API key with OCR access
- Google Sheets API credentials
- OpenAI API key

---

## 📂 Example Use Cases

- Automating expense reports
- Extracting invoice metadata for accounting
- Digitizing restaurant receipts for tax documentation

---

> Built with 💛 using [n8n](https://n8n.io) and [Mistral OCR](https://mistral.ai/).

