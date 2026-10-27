# E-Waste RecoveryAI

**AI-Based E-Waste Device and Component Detection with Circular Recovery & Reuse Recommendations**

E-Waste RecoveryAI is an AI-powered system designed to classify electronic waste, detect visible components, and recommend appropriate recovery pathways such as reuse, refurbishment, component harvesting, recycling, and safe disposal.

## Key Features

- **Device Classification:** Identifies electronic waste categories using computer vision.
- **Component Detection:** Detects visible components using YOLO-based object detection.
- **Recovery Recommendations:** Suggests reuse, repair, refurbishment, recycling, or special handling.
- **Confidence Scoring:** Reports model prediction confidence to help users assess results.
- **Value Estimation:** Supports estimated recovery and resale values in Indian Rupees (₹).
- **Web Interface:** Provides a user-facing interface built with React and Vite.
- **Backend API:** Uses FastAPI to support the analysis pipeline.

## Project Structure

- `frontend/` — React and Vite frontend.
- `web/` — Web assets and production interface.
- `src/` — Classification, detection, inference, and API modules.
- `mcp_server/` — Recovery rules and optimization logic.
- `demo/` — Sample electronic waste images.
- `tests/` — Automated tests.
- `docs/` — Dataset documentation, limitations, sources, and training guide.
- `reports/` — Generated evaluation reports and metrics.
- `train_all.py` — Training pipeline entry point.
- `EWaste_RecoveryAI_Training.ipynb` — Training notebook.
- `requirements.txt` — Python dependencies.

## Setup

Create and activate a Python environment, then install dependencies:

```bash
pip install -r requirements.txt
```

Start the FastAPI application:

```bash
python -m uvicorn src.api:app --reload --host 127.0.0.1 --port 8000
```

Open `http://127.0.0.1:8000` in your browser.

## Frontend Development

```bash
cd frontend
npm install
npm run dev
```

## Model Training

Review `docs/training_guide.md` and `docs/datasets.md` before training. If the required datasets and dependencies are available, use:

```bash
python train_all.py --all
```

## Testing

Run the automated tests with:

```bash
pytest tests/ -v
```

## Limitations

Predictions, component detections, confidence scores, and recovery valuations depend on model performance, image quality, and the available data. Estimated values are indicative, not guaranteed market prices. Components that cannot be reliably identified require manual inspection.

## References

Refer to `docs/sources.md` for the project's documented sources and `docs/limitations.md` for known limitations.

---

**Project:** E-Waste RecoveryAI  
**Focus:** AI, computer vision, electronic waste management, and circular economy.
