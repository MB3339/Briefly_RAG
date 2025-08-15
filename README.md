# ReportFindings-RAG (Multimodal)

Multimodal RAG for **report-style PDFs** (surveys, trend/trust reports).  
**Retrieval:** TF-IDF + section boosting + CLIP (text+images).  
**Answering:** Gemini 1.5 (multimodal) with page hints.  
Includes a chart-aware path for figure-heavy PDFs.

## Quickstart
1) `pip install -r requirements.txt`
2) Copy `.env.example` → `.env`, set `GOOGLE_API_KEY`, `PDF_PATH`, and (optional) `OUTPUT_DIR`
3) Open `notebooks/ReportFindings_RAG.ipynb` and run the cells:
   - Process PDF → Retrieve → Ask (`answer` for narrative, `answer_charts_ok` for charts)
   - Use `ask_and_save(...)` to export **.md / .json / .png** to `OUTPUT_DIR`

> Evaluation (Hit@k / MRR) is planned as a future addition.

## Example
![summary](assets/amplify_summary.png)

**Note:** Public, non-sensitive PDFs only. Do not commit API keys or PDFs.
