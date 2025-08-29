# ISCP_PII_DEFENSE_2.0
Project Guardian 2.0 PII detection and redacting tool along with deployment proposal




This repository contains a Python-based solution to detect and redact PII from CSV data streams.

### Files:

- `Detector_sai_pranavi.py`: This is the ,ain PII detector and redacting script. It is written to works in google Colab, Jupyter, as well as a plain Python script.
- `iscp_pii_dataset_-_Sheet1.csv`: Example input CSV file I've used
- `redacted_output_uploaded.csv`: Example output that was generated after running my script.
- `Deployment_proposal.md`: Proposed deployment strategy for production.

### Usage:

**Google Colab / Jupyter Notebook**
1. Upload `Detector_sai_pranavi.py`.
2. Run the script.
3. Upload your own CSV or test data when you are prompted to.
4. The redacted CSV `redacted_output_uploaded.csv` will be generated and the final codde snippet will download it into your system.

**Command-Line Python**
```bash
python Detector_sai_pranavi.py iscp_pii_dataset_-_Sheet1.csv
