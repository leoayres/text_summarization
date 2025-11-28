

# 📝 DOCX Text Summarizer using Hugging Face Transformers

This project allows you to **read `.docx` files**, automatically **summarize their content** using Hugging Face Transformers’ *summarization pipeline*, and **save the generated summary into a `.txt` file**.

It is ideal for quickly producing summaries of long documents such as reports, research papers, contracts, or academic texts.

---

## 🚀 Features

* Reads **.docx** documents
* Generates summaries using the **Hugging Face summarization pipeline**
* Configurable parameters:

  * `max_length`
  * `min_length`
  * `do_sample`
* Saves summaries to a **.txt** file
* Simple, clean, and easy-to-customize code

---

## 🛠️ Requirements

Install the required dependencies:

```bash
pip install python-docx transformers
```

> Note: Some summarization models may require PyTorch or TensorFlow to be installed.

---

## 📂 Code Overview

* **`read_docx()`**
  Reads and extracts text from a `.docx` file.

* **`summarize_text()`**
  Uses the Hugging Face **summarization pipeline** to generate a summary.

* **`save_summary_to_txt()`**
  Writes the summary to a `.txt` file.

* **Main execution block**
  Reads `documento.docx`, summarizes the content, and saves the output as `resumo.txt`.

---

## ▶️ How to Use

1. Place the `.docx` file you want to summarize in the same directory as the script.
2. Update the input filename if needed:

```python
docx_path = 'documento.docx'
```

3. Run the script:

```bash
python summarizer.py
```

4. The file **resumo.txt** (summary.txt) will be generated automatically.

---

## 🧠 Example Usage

```python
full_text = read_docx("input.docx")
summary = summarize_text(full_text, max_length=200, min_length=50)
save_summary_to_txt(summary, "summary.txt")
```

---

## 📌 Notes

* The default model used by `pipeline("summarization")` may vary depending on your Transformers version.
* For very long texts, consider splitting the content into smaller chunks before summarizing.
* `max_length` and `min_length` directly affect the summary’s size and quality.

---

## 📄 License

This project is licensed under the MIT License.
Feel free to use, modify, and contribute.


