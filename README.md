# Task 2 - Advanced Phishing Email Analysis with Header Examination

## Objective
To analyze a suspicious email sample and identify phishing indicators using content analysis and header examination techniques.

---

## Sample Email Summary

Subject: Urgent: Your Account Has Been Suspended!
Sender: security@paypa1.com

The email claims unusual activity and asks the user to verify the account within 24 hours using a provided link.

---

# Part 1: Content-Based Phishing Indicators

## 1. Spoofed Sender Domain
Sender address:
security@paypa1.com

Issue:
The letter "l" in paypal.com is replaced with the number "1".
This is a typosquatting technique used to impersonate legitimate domains.

---

## 2. Fear and Urgency Tactics
Subject:
"Urgent: Your Account Has Been Suspended!"

The email uses fear-based social engineering to pressure the user.

---

## 3. Suspicious Link
http://paypal-account-verification-secure.com/login

Issues:
- No HTTPS encryption
- Domain mismatch (not paypal.com)
- Misleading and overly long URL

---

## 4. Generic Greeting
"Dear Customer"

Legitimate companies usually address users by name.

---

# Part 2: Email Header Analysis

## Sample Header (Simulated for Analysis)

Received: from unknown-server.ru (185.234.219.10)
by mail.paypal.com
Return-Path: security@paypa1.com
SPF: FAIL
DKIM: NONE
Authentication-Results: spf=fail

---

## Header-Based Phishing Indicators

### 1. Suspicious Sending Server
The email originated from:
185.234.219.10 (unknown-server.ru)

This does not match PayPal’s official mail servers.

---

### 2. SPF Failure
SPF: FAIL

SPF (Sender Policy Framework) verifies whether the sending server is authorized.
Failure indicates spoofing attempt.

---

### 3. Missing DKIM
DKIM: NONE

DKIM digitally signs legitimate emails.
Absence of DKIM suggests unauthenticated email.

---

### 4. Domain Mismatch
Return-Path uses paypa1.com instead of paypal.com.
This confirms sender spoofing.

---

# Social Engineering Techniques Identified

- Domain impersonation
- Typosquatting
- Fear-based manipulation
- Urgency pressure
- Brand impersonation
- Credential harvesting attempt

---

# Conclusion

The email demonstrates multiple phishing characteristics including spoofed domain, fake link, urgency tactics, suspicious sending server, SPF failure, and missing DKIM authentication.

Both content analysis and header examination confirm that the email is a phishing attempt designed to steal user credentials.

---

# Key Learning

- Always inspect sender domain carefully.
- Verify SPF and DKIM authentication.
- Never click suspicious links.
- Check email headers using online analyzers.
- Confirm suspicious emails directly via official websites.
