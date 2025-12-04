# Image Data Extraction with OCR (Pandas)

## Project Overview

This notebook demonstrates a clean, production‑ready pipeline to extract tabular data from images using **Optical Character Recognition (OCR)**. Leveraging `pytesseract` (a Python wrapper for the Tesseract OCR engine) and `pandas`, the workflow covers:

1. **Dependency installation** – Python packages and the Tesseract binary.
2. **Image loading & visualization** – `Pillow` + `matplotlib`.
3. **OCR extraction** – converting the image into raw text.
4. **Data cleaning & structuring** – turning the raw OCR output into a tidy `DataFrame`.
5. **Optional advanced extraction** – `easyocr` for complex table layouts.

The notebook is fully documented, masks any sensitive file paths, and follows industry‑standard coding practices (type hints, error handling, reproducibility). It serves as a showcase for data‑engineering and data‑science roles that require **image‑to‑tabular data transformation**.

---

## Tech Stack

| Category | Tools |
|---|---|
| **Programming** | Python 3.12 |
| **OCR Engine** | Tesseract OCR (installed via Homebrew/apt/Windows installer) |
| **Python Wrapper** | `pytesseract` |
| **Image Handling** | `Pillow`, `matplotlib` |
| **Data Manipulation** | `pandas` |
| **Optional Advanced OCR** | `easyocr` |
| **Version Control** | Git (GitHub) |

---

## Workflow

```mermaid
graph LR
    A[Install Packages & Tesseract] --> B[Load Image]
    B --> C[Display Image (matplotlib)]
    C --> D[Run OCR (pytesseract)]
    D --> E[Clean Raw Text]
    E --> F[Parse to pandas DataFrame]
    F --> G[Export CSV / Excel]
    G --> H[Optional: EasyOCR for Complex Tables]
```

### Detailed Steps

1. **Install Packages** – `!pip install pytesseract pillow pandas` (run once).  
2. **Install Tesseract OCR** – see the **Installation** section below for OS‑specific commands.  
3. **Load & Visualize** – `Image.open(<PATH>)` and `plt.imshow`.  
4. **OCR Extraction** – `pytesseract.image_to_string(img)`.  
5. **Cleaning** – strip whitespace, split lines, handle empty rows.  
6. **Parsing** – use `pandas.read_fwf` or custom regex to convert fixed‑width columns into a DataFrame.  
7. **Export** – `df.to_csv('output/table_extracted.csv', index=False)` for downstream analysis.  
8. **Advanced** – replace step 4 with `easyocr.Reader(['en']).readtext(image_path)` for multi‑language or heavily formatted tables.

---

## Key Skills Demonstrated

- **OCR & Image Processing** – extracting structured data from unstructured visual sources.  
- **Data Cleaning** – handling noisy OCR output, whitespace normalization, and column alignment.  
- **Pandas Data Engineering** – converting raw strings into tidy DataFrames, exporting to CSV/Excel.  
- **Cross‑Platform Setup** – installing system‑level dependencies (Tesseract) alongside Python packages.  
- **Documentation & Reproducibility** – clear markdown cells, version‑controlled notebook, and masked file paths.

---

## Business Applications

| Use‑Case | Value Proposition |
|---|---|
| **Invoice & Receipt Processing** | Automate extraction of line‑item tables for accounting. |
| **Survey Form Digitization** | Convert scanned questionnaire tables into analyzable datasets. |
| **Legacy Report Migration** | Bring historic printed tables into modern data pipelines. |
| **Compliance Audits** | Quickly validate tabular data from scanned regulatory documents. |

---

## Technical Highlights

- **Masked File Paths** – placeholder `<PATH_TO_YOUR_IMAGE>` ensures no hard‑coded personal directories.  
- **Robust Error Handling** – `try/except` blocks (not shown) can capture missing Tesseract binaries.  
- **Optional EasyOCR** – one‑line switch for more sophisticated table structures.  
- **Export Flexibility** – CSV, Excel, or JSON output with a single `pandas` command.  
- **Reproducible Environment** – `requirements.txt` (generated via `pip freeze > requirements.txt`) captures exact package versions.

---

## Future Enhancements

- **Batch Processing** – loop over a directory of images, aggregate results into a master DataFrame.  
- **Post‑Processing Validation** – schema checks (e.g., column data types, range validation) using `pandera`.  
- **Hybrid PDF Conversion** – convert scanned PDFs to images (`pdf2image`) before OCR.  
- **Model Fine‑Tuning** – train a custom Tesseract language model for domain‑specific fonts.  
- **Interactive Dashboard** – expose the extraction pipeline via a Streamlit app for non‑technical users.

---

## Lessons Learned

1. **Image Quality Matters** – high‑resolution, low‑noise scans dramatically improve OCR accuracy.  
2. **Pre‑Processing Improves Results** – simple binarization or deskewing can boost character recognition.  
3. **Consistent Column Widths** – fixed‑width tables are easier to parse; otherwise, regex or `tabula-py` may be needed.  
4. **System Dependency Awareness** – always verify Tesseract is on the system `PATH` before running the notebook.  
5. **Graceful Degradation** – fallback to `easyocr` when `pytesseract` struggles with complex layouts.

---

## Related Projects

- **CSV → PostgreSQL ETL Pipeline** – data ingestion and storage best practices.  
- **Customer Mall Spending Analysis** – pandas‑based analytics on structured CSV data.  
- **HuggingFace NLP Analysis** – advanced text processing and sentiment analysis.

---

## Contact & Collaboration

**Author:** Akbar Basha  
**GitHub:** [@AkbarDev](https://github.com/AkbarDev)  
**LinkedIn:** [Connect with me](https://linkedin.com/in/akbarbasha)  

---

## License

This notebook is part of an internship portfolio and is provided for educational purposes under the MIT License.

---

## Acknowledgments

- **Tesseract OCR** – open‑source OCR engine maintained by Google.  
- **pytesseract** – Python wrapper simplifying OCR integration.  
- **EasyOCR** – optional deep‑learning based OCR for challenging layouts.
