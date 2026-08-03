
# Breach Intelligence Analyzer

## Overview

The **Breach Intelligence Analyzer** is a simple application that uses an AI model to evaluate the security strength of a user-provided password.

Instead of relying solely on traditional password validation rules, the application prompts an AI model to act as a **security auditor**. The AI analyzes the password, estimates its risk of being compromised, and returns:

* A **security risk score** from **1 to 100**
* A **written security assessment** explaining the password's strengths and weaknesses

The application then displays the AI-generated report to the user.

---

## Problem

Weak passwords remain one of the leading causes of compromised online accounts. Many users create passwords that are:

* Too short
* Easy to guess
* Based on dictionary words
* Reused across multiple services
* Missing complexity

Traditional password checkers typically verify only fixed rules such as length and character variety. They often fail to explain *why* a password is risky in plain language.

The Breach Intelligence Analyzer addresses this problem by leveraging an AI model to provide a more detailed, human-readable security assessment.

---

## How It Works

1. The user launches the application.
2. The application prompts the user to enter a password.
3. The password is sent to an AI model along with system instructions directing the model to act as a professional security auditor.
4. The AI evaluates the password and returns:

   * A risk score between **1 (very weak)** and **100 (very strong)**.
   * A written report describing:

     * Password strengths
     * Password weaknesses
     * Potential security risks
     * Suggestions for improvement
5. The application prints the score and report to the console.

---

## Example

### Input

```text
Enter password:
password123
```

### Output

```text
Risk Score: 22/100

Security Report:
This password is considered weak because it contains a common dictionary word
combined with predictable numbers. It would be vulnerable to dictionary and
credential-stuffing attacks. Consider using a longer passphrase with random
words, numbers, and special characters.
```

---

## How to Run

### Prerequisites

* Python 3.10 or later
* An OpenAI API key
* Required Python packages installed

### Installation

Clone the repository:

```bash
git clone https://github.com/koffi763/breach-intelligence-analyzer.git
```

Navigate to the project directory:

```bash
cd breach-intelligence-analyzer
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Set your OpenAI API key:

**Linux/macOS**

```bash
export OPENAI_API_KEY="your_api_key"
```

**Windows (Command Prompt)**

```cmd
set OPENAI_API_KEY=your_api_key
```

Run the application:

```bash
python main.py
```

Enter a password when prompted to receive an AI-generated risk assessment.

---

## Limitations

* The AI's evaluation is based on language model reasoning and should not be treated as a definitive security assessment.
* The application does not verify whether the password has appeared in known public data breaches.
* Passwords are transmitted to an external AI service for analysis. Sensitive or real production passwords should not be tested unless your organization's privacy and security policies permit it.
* The generated score is subjective and may vary slightly between requests.
* An internet connection and a valid OpenAI API key are required.

---

## Future Improvements

* Check passwords against known breach databases (e.g., Have I Been Pwned).
* Estimate password entropy mathematically.
* Add password generation recommendations.
* Build a web-based user interface.
* Provide downloadable security reports.
* Support batch analysis for multiple passwords.

---

## Disclaimer

This project is intended for educational purposes. It should not replace professional security auditing tools or enterprise password security solutions.
