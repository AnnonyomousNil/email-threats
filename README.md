# email-threats
Email Threats and Analysis

**Email phishing** is one of the most common ways to scam people in the modern digital age. An adversary can easily spoof an email, pretending to be someone else, or make an email tempting enough that the victim would get click-baited.

We will use a **sample phishing email** to analyze the threats these emails pose.

---

##  Sample Email Observations

### 1️ Suspicious Email Address
The email used in the attack is:
"info@dzetwehd.globalenterprises.pp.ua"


- This address looks suspicious due to the random key combinations.
- Official company emails rarely use such complex and obscure domains.
- Scammers often spoof trusted brands using look-alike domains.

---

### 2️ Deceptive Subject Line
Subject:  
"John - You have won a Lancôme Beauty Box"


- Claims to be from **Sephora**, a well-known beauty brand.
- Designed to **grab the victim's attention** immediately.
- Such messages are typically **too good to be true**, which is a red flag.

---

### 3️ Irrelevant Attachments
- Phishing emails often contain **irrelevant PDF/doc attachments**.
- These are often malware or used to lure the victim further.

---

### 4️ Suspicious Intent in the Email Body
- Claims to offer **free gifts**, **discounts**, or **instant rewards**.
- The email asks the user to **click a link** to claim a **Lancôme Beauty Box**.
- This is a common trick to lure victims into entering credentials on spoofed websites.

---

### 5️ Hover-to-Inspect Links
- Hovering over links reveals **redirect URLs**.
- Often the link will **not match** the brand it claims to be from.
- Scammers use **URL shorteners** or random domains to hide malicious destinations.
- Always inspect links before clicking and verify them using trusted tools.

---

### 6️ Poor Grammar and Spelling
- Many phishing emails have **grammatical errors** and **spelling mistakes**.
- This is a clear indicator of a scam.

---

## Using Email Headers to Identify Phishing

Email headers contain detailed **routing and authentication metadata**.

> Analyze headers using tools like [MxToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)

### Key Factors in Email Header Analysis:

#### SPF (Sender Policy Framework)
- Confirms whether the email server is **authorized** to send mail for the domain.

#### DKIM (DomainKeys Identified Mail)
- Checks whether the **email content has been altered** during transit.

#### DMARC (Domain-based Message Authentication, Reporting & Conformance)
- Aligns **SPF and DKIM** results to validate the authenticity of the email.

> If any of these checks fail, the email should be considered suspicious.

In our sample email:
- **DMARC and DKIM failed**, proving this is a phishing attempt.

---

## Summary Report

| # | Indicator | Description |
|---|-----------|-------------|
| 1 | Suspicious Email Address | `info@dzetwehd.globalenterprises.pp.ua` pretending to be a legitimate domain |
| 2 | Tempting Subject Line | "John - You have won a Lancôme Beauty Box" pretending to be from Sephora |
| 3 | Malicious Redirect Link | URL redirects to an unknown, spoofed website |
| 4 | Delayed Email Receipt | The sender path contains blacklisted addresses |
| 5 | Failed Authentication | DMARC and DKIM checks failed |

---

## Conclusion
This analysis demonstrates how phishing emails use deceptive techniques and spoofed identities. **Always inspect email headers and be skeptical of unexpected offers.** When in doubt, verify through official channels.


