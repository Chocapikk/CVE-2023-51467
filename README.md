# CVE-2023-51467 Scanner 🕵️‍♂️

## Description 📜

CVE-2023-51467 Scanner is a Python-based command-line tool 🛠️ that scans URLs for a specific vulnerability in the Apache OfBiz ERP system. This zero-day security flaw, tracked as CVE-2023-51467, allows attackers to bypass authentication protections due to an incomplete patch for the critical vulnerability CVE-2023-49070.

## Vulnerability Details 🔐

The CVE-2023-51467 vulnerability resides in the login functionality of Apache OfBiz versions prior to 18.12.10. It can be exploited by sending an HTTP request with empty or invalid USERNAME and PASSWORD parameters, which results in an authentication success message, allowing unauthorized access to internal resources.

## Installation 💻

To use the CVE-2023-51467 Scanner, you need Python 3.x.

You can install the required packages using `pip` 📦:

```shell
pip install -r requirements.txt 
```

## Usage 🚀

To scan a single URL 🎯:

```shell
python exploit.py -u http://example.com
```

To scan a list of URLs from a file 📊:

```shell
python exploit.py -f urls.txt -o output.txt -t 50
```

## Options ⚙️

- `-u`, `--url`: Single URL to send the GET request to 🌐.
- `-f`, `--file`: File containing a list of base URLs to scan 📄.
- `-o`, `--output`: File to write vulnerable systems to (default is `output.txt`) 📝.
- `-t`, `--threads`: Number of concurrent threads to use (default is 10) 🧵.

## Disclaimer ⚠️

This tool is intended for security research and should not be used for illegal activities. The authors of this tool cannot be held responsible for any misuse or damage from its use.