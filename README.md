# Phishing Email Investigation

## Project Overview

This project demonstrates a beginner-level phishing email investigation workflow using a fictional suspicious email. The objective is to identify potential phishing indicators, analyze email content, practice using cybersecurity tools, document evidence, and write an investigation summary.

The project simulates tasks that an entry-level Security Operations Center (SOC) Analyst may perform when reviewing a suspicious email.

**Case ID:** PHISH-001  
**Project Type:** Cybersecurity Portfolio Project  
**Investigation Type:** Simulated phishing investigation  
**Status:** Initial analysis documented; no real incident confirmed

## Objectives

- Identify common phishing characteristics in a suspicious email.
- Extract URLs and email addresses from email content.
- Practice email-header analysis.
- Review URL reputation results.
- Calculate a SHA-256 file hash using Windows PowerShell.
- Maintain an evidence register and IOC list.
- Document findings, limitations, and recommended actions.

## Tools Used

| Tool | Purpose |
|---|---|
| Notepad | Review sample email and create investigation documentation |
| Google Admin Toolbox Messageheader | Practice email-header analysis using a manually constructed header |
| CyberChef | Extract and normalize URLs and extract email addresses |
| VirusTotal | Practice interpreting URL reputation results using `example.com` |
| Windows PowerShell | Calculate a SHA-256 hash for the sample email file |
| File Explorer | Organize project files and evidence |

**Note:** urlscan.io was explored for practice, but it is not presented as a completed analysis unless its results are documented in the project.

## Project Structure

```text
Phishing-Email-Investigation/
├── 01_Sample_Email/
│   └── suspicious_email.txt
├── 02_Evidence/
│   ├── initial-observations.txt
│   └── evidence-register.txt
├── 03_Analysis/
│   ├── phishing-indicators.txt
│   ├── url-analysis.txt
│   ├── virustotal-url-analysis.txt
│   └── ioc-list.txt
├── 04_Reports/
│   └── investigation-summary.txt
├── 05_Portfolio/
└── README.md
```

The header analysis report, SHA-256 hash report, and any screenshots should also be retained in their actual project locations. Update this structure if those files are stored in different folders.

## Investigation Workflow

### 1. Email Review

Reviewed a fictional email with the subject:

`URGENT: Your Microsoft 365 Account Will Be Disabled`

Identified urgency, a threat of account suspension, an unverified sender identity, and an account-verification request as potential phishing characteristics.

### 2. URL Analysis with CyberChef

Used CyberChef to extract the URL from the sample email, normalize the defanged URL for analysis, and apply URL decoding.

The sample URL uses a reserved `.invalid` domain and was not visited.

### 3. Email-Address Extraction

Used CyberChef to extract the sender and recipient addresses from the fictional email.

### 4. Email-Header Analysis

Submitted a manually constructed practice header to Google Admin Toolbox Messageheader.

The tool displayed SPF, DKIM, and DMARC failures. Because the input was manually constructed, these results do not verify the authentication status of a genuine email.

### 5. URL Reputation Practice

Queried `example.com` in VirusTotal and observed a detection ratio of `0/92`.

This was a separate practice lookup. It does not represent a scan of the fictional phishing URL or prove that the fictional URL is malicious or safe.

### 6. SHA-256 File Hashing

Used Windows PowerShell's `Get-FileHash` command with the SHA-256 algorithm to calculate a hash for `suspicious_email.txt`.

The hash provides a fingerprint of the file's contents at the time of calculation. It does not independently establish whether the file is malicious.

### 7. Evidence and Reporting

Created an evidence register, phishing-indicator documentation, an IOC register, analysis reports, and an investigation summary to record observations and limitations.

## Key Findings

- The fictional email uses urgency and an account-suspension threat.
- The message contains a fictional account-verification URL.
- CyberChef successfully extracted the URL and email addresses from the sample.
- The practice header produced SPF, DKIM, and DMARC failure results.
- VirusTotal reported `0/92` detections for the separate practice domain `example.com`.
- SHA-256 hashing was used to fingerprint the saved sample email.

## Limitations

- The email and its indicators are fictional training data.
- The email header was manually constructed.
- The header authentication results are simulated, not verified results from a received email.
- The VirusTotal lookup was performed on `example.com`, not on the fictional phishing URL.
- No real malicious domain, IP address, compromised account, or phishing incident was confirmed.
- Tool output and extracted indicators alone do not prove malicious activity.

## Skills Demonstrated

- Phishing email triage
- Identification of common phishing indicators
- URL and email-address extraction
- Basic email-header analysis
- URL reputation lookup
- IOC documentation
- SHA-256 file hashing
- Evidence organization
- Security investigation reporting
- Technical documentation

## Conclusion

This project demonstrates a structured approach to reviewing a suspicious-looking email, using basic cybersecurity tools, documenting evidence, and communicating findings.

The exercise is a simulated investigation intended for learning and portfolio development. A real incident would require genuine email evidence, verified authentication results, and further investigation before reaching a final determination.

## Disclaimer

This project is for educational purposes only. The sample email, sender, recipient, URL, and practice header are fictional. The project does not claim to identify or confirm a real phishing attack.
