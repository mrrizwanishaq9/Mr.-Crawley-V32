# 🕷️ Mr. Crawley V32

### Web Crawler • OSINT Learning Tool • Website Explorer

**Mr. Crawley V32** is a lightweight Python command-line web crawler designed for learning how web crawling, URL discovery, website structure analysis, HTTP responses, and basic OSINT workflows work.

It can crawl publicly accessible pages, discover internal and external links, extract page titles, record HTTP status codes, collect basic response information, and export crawl results into multiple formats.

---

## ✨ Features

* 🌐 Public website crawling
* 🔗 Internal URL discovery
* 🌍 External-link detection
* 📄 Page title extraction
* 📡 HTTP status-code collection
* 📦 Content-Type detection
* 🧵 Configurable worker threads
* ⏱️ Configurable request delay
* ⌛ Request timeout control
* 🪪 Custom HTTP headers
* 🤖 `robots.txt` awareness
* 🔁 Duplicate URL filtering
* 📊 Crawl statistics
* 🛑 Graceful `Ctrl+C` stopping
* 💾 TXT report export
* 📋 CSV report export
* 🗂️ JSON report export
* 📱 Termux compatible
* 💻 Windows/Linux compatible
* 🐍 Single-file Python implementation

---

## 🖥️ Example Output

```text
╔══════════════════════════════════════════════════════════════╗
║                    MR. CRAWLEY V32                          ║
║             WEB CRAWLER & OSINT LEARNING TOOL               ║
╠══════════════════════════════════════════════════════════════╣
║  Public Web Crawler • URL Discovery • Export • Statistics   ║
╚══════════════════════════════════════════════════════════════╝

[+] Checking robots.txt...
[✓] robots.txt found

[+] Target : https://example.com
[+] Domain : example.com
[+] Threads: 5
[+] Delay  : 1.0s
[+] Max    : 50

────────────────────────────────────────────

[01] [200] https://example.com/
     Title: Example Domain
     Internal: 0 | External: 1

══════════════════════════════════════════════
              CRAWL SUMMARY
══════════════════════════════════════════════

Pages visited       : 1
URLs discovered     : 1
Internal links      : 0
External links      : 1
Successful results  : 1
Failed requests     : 0
Duplicates skipped  : 0
Elapsed time        : 1.78 sec

══════════════════════════════════════════════

[✓] Results saved:
    ├── mr_crawley_results.json
    ├── mr_crawley_results.csv
    └── mr_crawley_results.txt
```

---

## ⚙️ Requirements

* Python 3.9+
* `requests`
* `beautifulsoup4`

---

## 📦 Installation — Windows

Open PowerShell:

```powershell
py -m pip install requests beautifulsoup4
```

Check installation:

```powershell
py -c "import requests; import bs4; print('Dependencies OK')"
```

Expected:

```text
Dependencies OK
```

---

## 📱 Installation — Termux

Update packages:

```bash
pkg update
pkg upgrade
```

Install Python:

```bash
pkg install python
```

Install dependencies:

```bash
pip install requests beautifulsoup4
```

Check:

```bash
python -c "import requests; import bs4; print('Dependencies OK')"
```

---

## ▶️ Basic Usage

Windows:

```powershell
py MrCrawley_V32.py https://example.com
```

Termux:

```bash
python MrCrawley_V32.py https://example.com
```

---

## 🎛️ Advanced Options

### Maximum pages

```bash
python MrCrawley_V32.py https://example.com --max-pages 20
```

### Threads

```bash
python MrCrawley_V32.py https://example.com --threads 3
```

### Request delay

```bash
python MrCrawley_V32.py https://example.com --delay 2
```

### Timeout

```bash
python MrCrawley_V32.py https://example.com --timeout 15
```

### Custom output name

```bash
python MrCrawley_V32.py https://example.com --output my_scan
```

This creates:

```text
my_scan.json
my_scan.csv
my_scan.txt
```

### Combined example

```bash
python MrCrawley_V32.py https://example.com --max-pages 20 --threads 3 --delay 2 --timeout 10
```

---

## 🪪 Custom Headers

Mr. Crawley supports manually supplied HTTP headers for legitimate testing and development.

Example:

```bash
python MrCrawley_V32.py https://example.com --header "X-Test: 123"
```

Multiple headers can be supplied:

```bash
python MrCrawley_V32.py https://example.com --header "X-Test: 123" --header "X-Project: Crawley"
```

Only use headers in ways permitted by the target system and its policies.

---

## 📊 Export Formats

### JSON

Useful for Python programs and structured data processing.

```text
mr_crawley_results.json
```

### CSV

Useful for spreadsheets and data analysis.

```text
mr_crawley_results.csv
```

### TXT

Useful for simple readable reports.

```text
mr_crawley_results.txt
```

---

## 🧠 What You Can Learn

Mr. Crawley can be used as a practical learning project for:

* Python HTTP requests
* HTML parsing
* BeautifulSoup
* URL normalization
* URL discovery
* Web crawling concepts
* HTTP status codes
* HTTP headers
* Threading
* Request delays
* Error handling
* JSON/CSV file handling
* Command-line arguments
* OSINT methodology
* Basic website structure analysis

---

## 🏗️ Project Structure

```text
MrCrawley/
│
├── MrCrawley_V32.py
│
├── mr_crawley_results.json
├── mr_crawley_results.csv
├── mr_crawley_results.txt
│
└── README.md
```

The main crawler is intentionally kept in a **single Python file** so beginners can easily study and modify the code.

---

## 🔍 What Mr. Crawley Does

The basic workflow is:

```text
Target URL
     │
     ▼
robots.txt check
     │
     ▼
Download public page
     │
     ▼
Check HTTP response
     │
     ▼
Extract page title
     │
     ▼
Discover URLs
     │
     ├── Internal URLs
     │
     └── External URLs
     │
     ▼
Apply crawl limits
     │
     ▼
Save results
     │
     ├── JSON
     ├── CSV
     └── TXT
```

---

## 🛡️ Strong Educational Safety Disclaimer

**Mr. Crawley V32 is provided strictly for educational, research, defensive-security, and authorized web-analysis purposes.**

Use this software only against:

* Websites you own
* Systems you operate
* Your own test environments
* Public resources where crawling is permitted
* Systems for which you have explicit authorization

Do **not** use Mr. Crawley to:

* Gain unauthorized access
* Guess or attack passwords
* Attempt credential theft
* Bypass authentication or access controls
* Circumvent security protections
* Exploit vulnerabilities
* Collect private or restricted information
* Circumvent CAPTCHA or anti-bot mechanisms
* Overload or disrupt websites
* Conduct denial-of-service activity
* Evade rate limits
* Harass or invade another person's privacy
* Perform unlawful reconnaissance

Users are responsible for complying with applicable laws, website terms of service, access policies, privacy requirements, and organizational rules.

**A public URL does not automatically mean unlimited permission to crawl it.**

Keep crawl limits reasonable, respect `robots.txt` where applicable, use appropriate delays, and stop testing when authorization does not exist or is unclear.

The developer of Mr. Crawley is not responsible for misuse of the software.

---

## ⚠️ Responsible Crawling

Recommended beginner settings:

```text
Threads : 1–3
Delay   : 1–3 seconds
Pages   : 10–50
```

Start with a small page limit while learning.

For example:

```bash
python MrCrawley_V32.py https://example.com --max-pages 10 --threads 2 --delay 2
```

---

## 🧪 Safe Testing

For learning, begin with intentionally simple test targets such as:

```text
https://example.com
```

You can also create your own local HTML website and crawl it locally.

For example:

```text
http://127.0.0.1:8000
```

This provides a controlled environment where you own the target and can safely experiment with crawling behavior.

---

## 🐍 Technology

```text
Language       : Python
HTTP           : Requests
HTML Parsing   : BeautifulSoup
Concurrency    : Python Threading
Export         : JSON / CSV / TXT
Interface      : Command Line
Platform       : Windows / Linux / Termux
Version        : V32
```

---

## 🚀 Future Upgrade Ideas

Possible educational improvements for future versions:

```text
V33
 ├── Better crawl queue
 ├── Improved robots handling
 └── More detailed statistics

V34
 ├── Sitemap parsing
 ├── Link categorization
 └── Better reporting

V35
 ├── HTML report
 ├── Crawl visualization
 └── Improved terminal dashboard

V40
 ├── Modular architecture
 ├── Config file
 ├── Advanced reporting
 └── Local analytics dashboard
```

Future versions should continue to maintain reasonable crawling limits and authorization requirements.

---

## 📜 License

This project is intended as an educational cybersecurity/web-development learning project.

Before using it against a website or service, verify that your intended activity is permitted.

---

## 👨‍💻 Project

**Mr. Crawley V32**

> Crawl • Discover • Analyze • Learn

**Educational Web Crawling & OSINT Learning Tool**
