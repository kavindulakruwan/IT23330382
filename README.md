# Singlish to Sinhala Transliteration - Test Automation

**Student Name:** W.M.K. Lakruwan  
**IT Number:** IT23330382  
**Module:** IT3040 – ITPM  
**Assignment:** Assignment 1 – Option 1: Transliteration Accuracy Testing

---

## Project Overview

This project automates the testing of the **Chat Sinhala transliteration** function available at:  
https://www.pixelssuite.com/chat-translator

The test suite contains **50 negative test cases** that verify scenarios where the system fails to correctly convert chat-style Singlish input into Sinhala output. All 50 test cases cover the 24 Singlish input types specified in the assignment.

---

## Project Structure

```
D:\test_automation\
│
├── test_automation.py              # Main Playwright automation script
├── Assignment 1 - Test cases.xlsx  # Excel file with all 50 test cases
├── README.md                       # This file
```

---

## Prerequisites

- Python 3.11 or 3.12 — https://www.python.org/downloads/
- Google Chrome (recommended) — https://www.google.com/chrome/

---

## Installation

### Step 1 — Extract project

```
D:\test_automation\
```

### Step 2 — Open CMD

Win + R → cmd

### Step 3 — Navigate

```bash
cd /d D:\test_automation
```

### Step 4 — Install dependencies

```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

## How to Run Tests

```bash
python test_automation.py --excel "D:\test_automation\Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 8000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

---

### Command Parameters Explained

| Parameter | Value | Description |
|---|---|---|
| `--excel` | Path to Excel file | The test cases file to read from and write results to |
| `--url` | Translator URL | The live application URL being tested |
| `--wait-ms` | `8000` | Wait time (ms) for the UI to update after each input |
| `--type-delay-ms` | `80` | Delay (ms) between each keystroke when typing |
| `--slow-mo-ms` | `200` | Slow motion delay (ms) for browser actions |
| `--save-every` | `1` | Save results to Excel after every test case |
| `--keep-open` | — | Keeps the browser open after all tests finish |

> ⚠️ **Do NOT press CTRL+C** while the script is running. Let it complete fully. It will take approximately **10–15 minutes** for all 50 test cases.

---

## Checking Results

1. Wait for the script to finish running all 50 test cases
2. Open the file `Assignment 1 - Test cases.xlsx`
3. Check that the **Actual output** (Column E) and **Status** (Column F) columns are filled in for all 50 rows
4. Status will show either **Pass** or **Fail** for each test case

---

## Notes

- All 50 test cases are **negative test cases** (expected to Fail) as required by the assignment
- Test Case IDs follow the format `Neg_Fun_XXXX`
- Input length types: **S** (≤ 30 chars), **M** (31–299 chars), **L** (300–450 chars)
- Do **not** manually edit the **Actual output** or **Status** columns — these are written automatically by the script

