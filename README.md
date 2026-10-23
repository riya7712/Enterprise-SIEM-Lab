# Enterprise SIEM Lab: Security Log Monitoring and Alert Analysis

## Project overview
This beginner-friendly Python project demonstrates basic Security Information and Event Management (SIEM) concepts. It analyses a small synthetic security-log dataset, applies simple detection rules, produces alert summaries, and visualises the results.

**Important:** This is a Python log-analysis prototype, not a deployed Wazuh cluster. The sample records are fictional and are only for learning.

## Objectives
- Parse and explore structured security events.
- Detect repeated failed logins.
- Flag successful logins after repeated failures.
- Detect repeated blocked connections.
- Summarise alert severity and visualise alert counts.

## Dataset
The notebook creates a small synthetic dataset internally, so a separate dataset download is not required. The IP addresses use documentation/example ranges.

For optional future extension using real public research data, see the Canadian Institute for Cybersecurity's CIC-IDS2017 dataset:
https://www.unb.ca/cic/datasets/ids-2017.html

Review the dataset's terms and documentation before use.

## Technologies
- Python 3
- Jupyter Notebook
- pandas
- matplotlib

## Files
- `YourName_EnterpriseSIEMLab.ipynb` — code, explanations, sample data, detection rules, charts, and CSV export.
- `requirements.txt` — Python dependencies.
- `YourName_ProjectReport.docx` — project documentation.

## Setup and run
1. Install Python 3.10 or newer.
2. Open a terminal in this project folder.
3. Install dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Start Jupyter:

   ```bash
   jupyter notebook
   ```

5. Open `YourName_EnterpriseSIEMLab.ipynb`.
6. Choose **Run All** to execute the notebook from top to bottom.

The notebook creates a `siem_output` folder containing `sample_security_events.csv` and `detected_alerts.csv`.

## Detection rules
1. At least three failed logins for the same username from the same source IP.
2. A successful login after those repeated failures.
3. At least two blocked connections from the same source IP.

These simple rules are illustrative. Alerts are not proof of an attack and should be investigated with additional context.

## Limitations
- Synthetic data only; no live log collection.
- No deployed SIEM manager or dashboard.
- Rule-based detection only; no machine learning.
- No automated blocking or response.

## Future scope
Connect the prototype to authorised system logs, add time-window logic, test on a suitable labelled dataset, tune false positives, and integrate with a Wazuh lab.

## Author
Replace this line with your name, course/program, and submission date before submitting.
