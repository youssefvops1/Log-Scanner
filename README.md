# Log-Scanner
Log Exposure Scanner  A lightweight security auditing tool that scans local text files and log directories to detect potentially exposed service credentials or sensitive configuration entries.
The tool analyzes logs for patterns related to:

SMTP configurations (ports 25, 465, 587, 2525)

cPanel login formats

Webmail login entries

WHM access patterns

WordPress login references

Detected entries are categorized and exported into organized result files to help security researchers, developers, and system administrators quickly identify accidental credential leaks inside logs or data dumps.

⚠️ Important:
This project is intended only for defensive security auditing and educational purposes.
Use it only on systems and data you own or have explicit authorization to audit.

Features

Fast multi-threaded log scanning

Recursive directory scanning

Automatic categorization of detected entries

Real-time terminal statistics

Organized output files

Lightweight and easy to run

Installation
1. Clone the repository
bash
git clone https://github.com/yourusername/log-exposure-scanner.git
cd log-exposure-scanner
2. Install Python

Make sure Python 3.8 or newer is installed.
Check your version:
bash
python --version
3. Install requirements (if needed)
pip install -r requirements.txt
(Most versions require only standard Python libraries.)
Usage

Run the scanner:
bash
python scanner.py
You will be prompted to choose:
1 - Scan a single file
2 - Scan a folder recursively
hen drag & drop the path of the file or folder you want to analyze.

Example:
Select Option [1/2]: 2
Drag and Drop Path here: C:\logs
Output

Results are automatically saved inside:
DARKD3_Results/
Example files:
smtps.txt
cpanel.txt
webmail.txt
whm.txt
wordpress.txt
Each file contains detected entries related to that category.
