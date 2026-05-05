# Singlish Transliteration Testing

Playwright automation scripts for testing Chat Sinhala transliteration accuracy at [pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator) — IT3040 ITPM Assignment 1

---

## Prerequisites

- Python 3.11 or 3.12
- Google Chrome (recommended)

---

## Installation

**Step 1 — Clone the repository:**
```
git clone https://github.com/YOUR_USERNAME/Singlish-Transliteration-Testing.git
cd Singlish-Transliteration-Testing
```

**Step 2 — Install dependencies:**
```
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

## How to Run

**Step 1 — Place the Excel file in the same folder as the script:**

Place `Assignment_1_-_Test_cases.xlsx` in the same directory as `test_automation.py`. Make sure the following columns are filled:
- `Test Case ID` (e.g., Neg_0001)
- `Input length type` (S, M, or L)
- `Input` (Singlish text)
- `Expected output` (correct Sinhala output)

Do NOT fill in the `Actual output` or `Status` columns — these are filled automatically.

**Step 2 — Run the script:**
```
python test_automation.py --excel "Assignment_1_-_Test_cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

**Step 3 — Check results:**

After the script finishes, reopen the Excel file and verify that the `Actual output` and `Status` columns have been filled in automatically.

---

## Project Structure

```
Singlish-Transliteration-Testing/
├── Assighment 1_Test_cases      #test cases excle file
├── Assighment_1-Tesr_case.py     # Main Playwright automation script
└── README.md                 # Project documentation
```

---

## Notes

- Input length categories: **S** (≤ 30 characters), **M** (31–299 characters), **L** (300–450 characters)
- Only the **Chat Sinhala** transliteration function is tested
- Standard Sinhala, backend APIs, performance, scalability, and security testing are out of scope
