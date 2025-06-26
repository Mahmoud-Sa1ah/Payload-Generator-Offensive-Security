# Payload-Generator-Offensive-Security  
This is **Task 2** of the **IT Solera Cyber Department Summer Internship 2025**.  
A modular, Python-based payload generation tool designed to automate the creation of XSS, SQLi, and Command Injection payloads with encoding and evasion techniques for penetration testing.

---

## 📌 Features

| Module        | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| `--xss`       | Generates XSS payloads (reflected, stored, DOM-based) with bypass options   |
| `--sqli`      | Generates SQL Injection payloads (error-based, union, blind)                |
| `--cmd`       | Generates command injection payloads for Linux and Windows targets          |
| `--encode`    | Encodes payloads (Base64, URL, Unicode, HTML entity, Hex)                   |
| `--obfuscate` | Adds random obfuscation (comments, spacing, junk) to bypass filters         |
| `--output`    | Outputs payloads as JSON (`--output=json`) or prints to terminal (default)  |
| `--clipboard` | Copies the generated payloads directly to your clipboard                    |

---

## ⚙️ Installation

> **Requirements:**
- Python 3.10+
- `pyperclip` module (`pip install pyperclip`)
- PyCharm or any Python IDE

### 🔧 Setup Instructions:
1. Clone the repository or download the project files.
2. Open the project in your preferred editor.
3. Install dependencies:

```bash
pip install -r requirements.txt
Run the tool using:

bash
Copy
Edit
python main.py --xss --sqli --cmd --encode=url --clipboard --output=json
📁 Payload Sources
Payload templates are stored in the payloads/ directory:

xss.txt → XSS payloads

sqli.txt → SQL injection strings

cmd_injection.txt → Command injection commands

💡 Example Output
json
Copy
Edit
{
  "type": "xss",
  "raw": "<svg/onload=alert(1)>",
  "encoded": {
    "url": "%3Csvg%2Fonload%3Dalert%281%29%3E"
  }
}
