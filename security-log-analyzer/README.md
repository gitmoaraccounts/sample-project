# Overview 
Hi there! 👋

This repository contains a fake project to demonstrate technical writing and documentation skills. Everything below the Overview section is made up, which means the links won't go anywhere (except the Python one) and you won't be able to actually install anything.

## Log Analyzer Tool
Log Analyzer is a simple tool for security engineers and cloud administrators to analyze large volumes of security logs for common patterns:

* Impossible travel detections
* Multiple failed login attempts
* Suspicious IP addresses
* Privilege escalation events

The tool supports logs from:

✅ AWS CloudTrail\
✅ Azure Activity Logs\
✅ GCP Cloud Audit Logs


## Getting Started
### Pre-requisites
To install this tool, you'll need Python 3.9 or newer and a Windows, Mac, or Linux operating system. Additionally, any log files you want to analyze must be in JSON format, so place those logs somewhere easily accessible on your endpoint.

### Installation Steps 
>This guide does not cover installing Python. Please visit the official Python site: https://www.python.org/ to download and install for your particular operating system.

1: Clone the repository
``` bash
git clone https://github.com/<user>/security-log-analyzer.git
```
2: Change into the newly created repository
``` bash
cd security-log-analyzer
```
3: Add the below requirements.txt file to your folder
```bash
vim requirements.txt
# Copy paste requirements.txt into this new file
:x 
# Run :x in vim to save and close the file
```
#### requirements.txt
```
# Log parsing library
logparser==1.2.3

# IP reputation lookup utility
iplookup==0.4.1

# AWS CloudTrail analysis module
cloudtrail-analyzer==2.0.0

# Geolocation mapping tool
geoip-mapper==0.9.8

# Report generation library (CSV / HTML)
reportgen==3.5.7
```


4: pip install requirements.txt
``` bash
pip install -r requirements.txt
```


## Usage
After you complete the installation steps, run the following command to execute the tool:
``` bash
python analyzer.py --input logs.json --rules config/rules.yaml --output report.csv
```
The command options are:

| Argument      | Description |
| -----------   | ----------- |
| `--input`     | Path to JSON log file|
| `--rules`     | Path to YAML rules file|
| `--output`    | Path to CSV output file|
| `--ui`        | Generate a CLI output|

You can see the analysis results by opening the .csv file or by using the built in User Interface to see a better, human-readable version that easily summarizes the results. That command would be:

``` bash
python analyzer.py --input logs.json --rules config/rules.yaml --output report.csv --ui
```

#### Example CLI UI Output:
```
+-------------------------------------------------------------+
|                 SECURITY LOG ANALYZER v1.0                  |
+-------------------------------------------------------------+
| Input file: logs.json                                       |
| Ruleset: config/rules.yaml                                  |
| Output file: report.csv                                     |
+-------------------------------------------------------------+

Scanning logs... [##########] 100% complete

Summary of Findings:
--------------------
- Impossible Travel:         2 occurrences
- Multiple Failed Logins:    8 occurrences
- Privilege Escalation:      1 occurrence
- Suspicious IP Addresses:   3 occurrences

Detailed report written to report.csv

+-------------------------------------------------------------+
|                ANALYSIS COMPLETE - 4 alerts                 |
+-------------------------------------------------------------+
```

## Conclusion
Thanks for reading!