# Automated Employee Onboarding Document Processor

## Features
- Reads CSV and Excel (.xlsx/.xlsm) employee files.
- Validates required fields, employee IDs, duplicates and joining dates.
- Creates an employee-specific folder.
- Generates both onboarding.txt and onboarding.pdf.
- Produces a CSV processing report and an application log.
- Includes unit tests.

## Setup (Windows PowerShell)
Run from the project root:
```powershell
python -m pip install -r requirements.txt
python main.py
```

Run tests:
```powershell
python -m unittest discover -s tests -v
```

Use an Excel input:
```powershell
python main.py --input input/employees.xlsx
```

Required columns: `employee_id,name,department,role,joining_date,manager`

Accepted date formats: YYYY-MM-DD, DD-MM-YYYY, DD/MM/YYYY, MM/DD/YYYY, and Excel date cells.

## Output
- `output/EMP001_Anil_Kumar/onboarding.txt`
- `output/EMP001_Anil_Kumar/onboarding.pdf`
- `reports/processing_summary.csv`
- `logs/onboarding.log`

## Team split
Participant 1: validation, date parsing, template rendering, PDF generation.
Participant 2: file handling, folder automation, reports, logging, exceptions and tests.

Review generated documents before using them for real onboarding.
