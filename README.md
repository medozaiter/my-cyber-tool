# Web Vulnerability Scanner (SQLi & XSS)

> **Course Project:** Automated Web Application Security Testing  
> **Author:** Mustafa AbuZaiter  

---

## 📋 Overview
This project is an automated web application vulnerability scanner developed as part of the academic requirements for the security course. The tool is designed to identify common security flaws in web applications, specifically **SQL Injection (SQLi)** and **Reflected Cross-Site Scripting (XSS)**.

### Objectives
- Automate the process of discovering form inputs and URL parameters.
- Detect Error-Based SQL Injection vulnerabilities through signature matching.
- Detect Reflected XSS vulnerabilities by validating input reflection and sanitation.
- Provide a clear report of discovered vulnerabilities for remediation.

---

## 🛠 Architecture & Workflow

The scanner follows a modular architecture divided into four main layers:

1. **Crawler & Parser (`crawler.py`):** Extracts forms, parameters, and inputs using `BeautifulSoup4`.
2. **SQLi Engine (`sqli_scanner.py`):** Injects SQL payloads and analyzes HTTP responses for database error patterns.
3. **XSS Engine (`xss_scanner.py`):** Injects JavaScript payloads and checks for unsanitized reflection in the DOM.
4. **Core Controller (`cli.py` / `main.py`):** Handles user input via CLI and orchestrates the scanning sequence.

### Workflow Diagram
