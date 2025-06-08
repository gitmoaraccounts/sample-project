# Overview 
Hi there! 👋

This repository contains a fake project to demonstrate technical writing and documentation skills. Everything below the Overview section is made up, which means the links won't go anywhere (except the Python one) and you won't be able to actually install anything.

## Log Analyzer Tool - Overview
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

>This guide does not cover installing Python. Please visit the official Python site: https://www.python.org/ to download and install for your particular operating system.


### Installation Steps 
1: Clone the repository\
2: Change into the newly created repo\
3: Add the below requirements.txt file to your folder\
4: pip install requirements.txt

The commands for each step are below for reference. Note after running `vim requirements.txt`, you can copy the contents of the provided requirements.txt file into your newly created one.

``` bash
git clone https://github.com/<user>/security-log-analyzer.git
cd security-log-analyzer
vim requirements.txt 
pip install -r requirements.txt
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
## Usage
After you completed the installation steps, run the following command to execute the tool:
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

You can see the analysis results in the .csv file or use the built in User Interface to see a better, human-readable version that easily summarizes the results. That command would be:

```
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