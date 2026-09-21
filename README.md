# IBAN Bulk Validator

A command-line Python automation script that reads a list of International Bank Account Numbers (IBANs) from a text file, validates them via web automation scraping, and outputs a sanitized verification log.

## Overview

**IBAN Bulk Validator** streamlines bank account auditing by parsing flat-file lists of IBANs and programmatically validating them against a reliable checker platform (`iban-rechner.de`). Utilizing `requests` and `BeautifulSoup4`, it evaluates the structural integrity of each line, outputs real-time color-coded console logs, and builds an active record tracking successfully validated credentials with custom timestamps.

## Features

- **Bulk Input Processing:** Reads raw `.txt` inputs line-by-line using absolute path parameters to process entire account listings concurrently.
- **Asynchronous Scraping Engine:** Employs form payload parsing pipelines to scrape results directly from verification fieldsets without full browser automation overhead.
- **Color-Coded Terminal Feedback:** Integrates standard ANSI color escapes to instantly flash real-time success logs (**Green** for Correct) and connection exceptions (**Red** for Invalid or Missing fields).
- **Automated Logging Node:** Creates an accompanying outputs file (`*_checked.txt`) in your source directory, preserving a permanent execution timestamp and valid record configurations.
- **Rate-Limit Polling Protections:** Implements incremental 3-second sleep deltas between network requests to protect endpoint boundaries from request flood blockages.

## Tech Stack

- **Language:** Python 3.9 or higher
- **Network Pipeline:** Requests
- **Parsing Toolkit:** BeautifulSoup4 (HTML Parser)

## Project Structure

```bash
ibans-bulk-checking-script/
├── script.py              # Core execution automation script
├── test.txt              # Testing data
├── requirements.txt     # Python dependency environment package index
└── README.md            # Script usage and technical overview documentation
```

## Setup & Execution

### Prerequisites

- Python 3.7+ installed on your host machine.
- An active internet connection to poll validation data endpoints.

### Installation

- Clone or download this automation directory cleanly:

  ```bash
  git clone https://github.com
  ```

- Navigate to the project path and install the tracking library dependencies:
  ```bash
  pip install -r requirements.txt
  ```

### Usage Instructions

1. Prepare a standard text file (e.g., `accounts.txt`) containing one IBAN per line.
2. Launch the script directly from your terminal console:
   ```bash
   python main.py
   ```
3. Input the absolute path to your file when prompted, making sure to format folder paths using forward slashes (e.g., `C:/Users/Name/Documents/accounts.txt`).
4. Press **ENTER** to execute. Once complete, inspect the newly generated `_checked.txt` output file inside your target folder.

## Author

H2SO4-1191 – Software Engineer
