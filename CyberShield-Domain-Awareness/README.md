<div align="center">

<!-- HEADER BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,30:003366,70:00ff88,100:0d1117&height=220&section=header&text=CyberShield&fontSize=72&fontColor=ffffff&fontAlignY=38&desc=Domain%20Attack%20Awareness%20Platform&descSize=20&descColor=00ff88&descAlignY=60&animation=fadeIn" width="100%"/>

<br/>

<!-- BADGES -->
![Made With](https://img.shields.io/badge/Made%20With-HTML%20%7C%20CSS%20%7C%20JS-00ff88?style=for-the-badge&logo=html5&logoColor=white)
![Security Awareness](https://img.shields.io/badge/Purpose-Security%20Awareness-E24B4A?style=for-the-badge&logo=shield&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-0d8a6f?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)
![Author](https://img.shields.io/badge/Author-Kiran%20Kumar%20K-003366?style=for-the-badge&logo=github&logoColor=white)

<br/>

> **⚠️ For Security Awareness & Education Only — Do NOT misuse this knowledge.**

</div>

---

## 🛡️ What is CyberShield?

**CyberShield** is a fully interactive, single-file cybersecurity awareness web platform designed to educate developers, security teams, end users, and students about **phishing**, **domain spoofing**, **typosquatting**, and **payment fraud attacks**.

Built after seeing real-world losses from one-click phishing attacks, this tool makes complex attack concepts tangible — with live demos, interactive quizzes, a domain risk detector, and real financial impact data.

```
┌──(kiran㉿iisc-bangalore)-[~/CyberShield-Domain-Awareness]
└─$ cat mission.txt

  Target    :  Reduce phishing click rates through interactive education
  Method    :  Show, don't tell — live domain demos + quiz + detector
  Audience  :  Devs · SOC Teams · Finance Teams · General Users
  Stack     :  Pure HTML + CSS + Vanilla JS — zero dependencies
  Status    :  Active · Open for contributions
```

---

## ✨ Features

| Feature | Description |
|--------|-------------|
| 🔴 **8 Attack Pattern Cards** | Homoglyph, Typosquatting, Subdomain Abuse, TLD Swap, Keyword Injection, IDN/Unicode, Billing Scams, Display Name Spoofing |
| 📊 **Financial Impact Dashboard** | Animated counters, real loss statistics, per-incident cost breakdowns |
| 📧 **Real vs. Phishing Email Demo** | Side-by-side visual comparison with verdict labels |
| 🔍 **Live Domain Risk Detector** | Heuristic analysis tool — paste any domain and get instant risk scoring |
| 🧠 **5-Question Interactive Quiz** | Test your ability to spot phishing domains with live feedback |
| ⚖️ **Real vs. Fake Comparison Table** | Quick-reference across all 7 attack types |
| 🗓️ **Payment Scam Timeline** | Step-by-step story of how an $85K wire fraud unfolds |
| ✅ **Defender Checklist** | Actionable steps for Email Security, Developers, SOC Teams & End Users |
| 🌐 **Golden Domain Rule Visual** | Interactive diagram showing how to identify the real domain in any URL |
| 🎨 **Fully Responsive Design** | Works on desktop and mobile — no external dependencies |

---

## 🎯 Who Is This For?

```
👨‍💻  Developers         →  Learn secure domain validation patterns
🛡️   SOC / IR Teams     →  Use as awareness training material
💼   Finance Teams       →  Understand BEC and invoice fraud mechanics
🎓   Students / CTF      →  Study real phishing attack vectors
🏢   Organizations       →  Deploy internally for security awareness
```

---

## 🚀 Quick Start

No installation. No dependencies. Just open it.

```bash
# Clone the repository
git clone https://github.com/kirankumark-sec/CyberShield-Domain-Awareness.git

# Navigate into the project
cd CyberShield-Domain-Awareness

# Open directly in your browser
open index.html
# or on Linux:
xdg-open index.html
```

> ✅ Works completely offline. No Node.js, no npm, no build tools required.

---

## 🔍 Attack Patterns Covered

<details>
<summary><b>01 — Homoglyph Attacks (Character Substitution)</b></summary>

Characters that look visually identical but are different code points.

```
microsoft.com      ✅ Real
rnicrosoft.com     ❌ Fake  (rn → looks like m)
micros0ft.com      ❌ Fake  (0 → replaces o)
microsоft.com      ❌ Fake  (Cyrillic о — visually identical)
```

</details>

<details>
<summary><b>02 — Typosquatting (Missing / Extra Characters)</b></summary>

Banking on users making natural keyboard errors.

```
paypal.com         ✅ Real
paypai.com         ❌ Fake  (i instead of l)
paypaI.com         ❌ Fake  (capital I instead of l)
paypa11.com        ❌ Fake  (double l)
```

</details>

<details>
<summary><b>03 — Subdomain Abuse</b></summary>

Brand name used as a subdomain. The real domain is after the last dot.

```
login.microsoft.com             ✅ Real  →  microsoft.com owns this
microsoft.login-secure.com      ❌ Fake  →  login-secure.com owns this!
```

</details>

<details>
<summary><b>04 — TLD Abuse (Wrong Top-Level Domain)</b></summary>

Swapping .com for a lookalike TLD.

```
amazon.com    ✅ Real
amazon.co     ❌ Fake
amazon.in     ❌ Suspicious
amazon.net    ❌ Fake
```

</details>

<details>
<summary><b>05 — Security Keyword Injection</b></summary>

Adding panic-inducing words to make URLs seem official.

```
apple-secure.com              ❌  Legit companies don't do this
apple-verify-account.com      ❌
apple-login-alert.net         ❌
```

</details>

<details>
<summary><b>06 — Unicode / IDN Homograph Attacks</b></summary>

Internationalized Domain Names use non-Latin Unicode that renders identically.

```
google.com      ✅ Real   (all Latin characters)
gоogle.com      ❌ Fake   (Cyrillic о — U+043E)
gοogle.com      ❌ Fake   (Greek ο — U+03BF)
```

> 🚨 These are **visually indistinguishable** to the naked eye. Extremely dangerous.

</details>

<details>
<summary><b>07 — Billing & Payment Scam Domains</b></summary>

Targeting finance teams with fake invoice and renewal emails.

```
netflix-billing.com       ❌
netflix-invoice.net       ❌
netflix-renewal.org       ❌
```

</details>

<details>
<summary><b>08 — Display Name Spoofing</b></summary>

The display name says `PayPal Support` but the actual sender domain is fake.

```
alerts@paypal.com                   ✅ Real
alerts@paypa1-secure.net            ❌ Fake — check the domain, not the name
```

</details>

---

## 🧠 The Golden Rule

```
✅  login.microsoft.com         →  microsoft.com  (safe — subdomain of real domain)
❌  microsoft.login-alert.com   →  login-alert.com  (ATTACKER'S domain!)
```

**Always read the domain right-to-left from the first `/` — the registrable domain is the last two parts.**

---

## 🛠️ Developer Defense Patterns

```python
# ❌ UNSAFE — Never use substring matching
if "paypal" in email_domain:
    trust_email()

# ✅ SAFE — Always exact match or allowlist
TRUSTED_DOMAINS = {"paypal.com", "paypal.co.uk"}
if email_domain in TRUSTED_DOMAINS:
    trust_email()
```

```javascript
// ❌ UNSAFE
if (domain.includes("microsoft")) { ... }

// ✅ SAFE
const ALLOWED = new Set(["microsoft.com", "live.com"]);
if (ALLOWED.has(domain)) { ... }
```

---

## 💸 Real Financial Impact

| Stat | Value |
|------|-------|
| Global cybercrime losses (2023) | **$12.5 Billion** |
| Average BEC loss per incident | **$36,000** |
| Time to detect phishing breach | **197 days** |
| Daily phishing emails sent | **3.4 Billion** |
| Organizations targeted (2023) | **76%** |
| Breaches starting with phishing | **90%** |

---

## 📁 Project Structure

```
CyberShield-Domain-Awareness/
│
├── index.html          # Complete single-file platform (HTML + CSS + JS)
├── README.md           # You are here
└── LICENSE             # MIT License
```

---

## 📸 Preview

> Open `index.html` in your browser to see the full interactive platform.

**Sections inside:**
- 🔴 Hero with live stats
- 📊 Financial impact banner with animated counter
- 🃏 8 attack pattern cards with real/fake domain comparisons
- 📧 Phishing email comparison demo
- 🔍 Live domain risk detector (try `paypa1.com` or `microsoft-login-secure.com`)
- ✅ Defender checklist for developers, SOC teams & users
- 📆 Wire fraud timeline walkthrough
- 🧠 5-question phishing awareness quiz

---

## 🤝 Contributing

Contributions are welcome! If you have new attack patterns, better quiz questions, or improved detection logic:

```bash
# Fork → Clone → Create branch → Make changes → Push → PR
git checkout -b feature/new-attack-pattern
git commit -m "feat: add combo-squatting examples"
git push origin feature/new-attack-pattern
```

---

## 🏆 Author

<div align="center">

[![Author Banner](https://capsule-render.vercel.app/api?type=rect&color=0:0d1117,100:003366&height=80&text=Kiran%20Kumar%20K&fontSize=28&fontColor=00ff88&desc=Ethical%20Hacker%20%7C%20VAPT%20Specialist%20%7C%20IISc%20Bangalore&descColor=ffffff&descSize=13)](https://github.com/kirankumark-sec)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-kiran--kumar--k3-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/kiran-kumar-k3)
[![GitHub](https://img.shields.io/badge/GitHub-kirankumark--sec-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/kirankumark-sec)
[![Blog](https://img.shields.io/badge/Blog-kirankumark3-FF5722?style=for-the-badge&logo=blogger&logoColor=white)](https://kirankumark3.blogspot.com)
[![Bugcrowd](https://img.shields.io/badge/Bugcrowd-NASA%20Disclosure-F26822?style=for-the-badge&logo=bugcrowd&logoColor=white)](https://bugcrowd.com/disclosures/fb4354a1-3cd8-4395-a619-2ae39b986c5f/)
[![Gmail](https://img.shields.io/badge/Gmail-kirankumark.sec-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kirankumark.sec@gmail.com)

**Junior Security Analyst · IISc DIGITS/ISO, Bangalore**  
Ethical Hacker · VAPT Specialist · Bug Bounty Hunter · CTF Player  
Public Disclosures: NASA · Stanford · Govt Portals

</div>

---

## ⚖️ Legal Disclaimer

```
⚠️  THIS PROJECT IS FOR EDUCATIONAL AND SECURITY AWARENESS PURPOSES ONLY.

All domain examples shown in this platform are for DEFENSIVE awareness only.
They are provided to help security professionals, developers, and users
recognize and defend against phishing attacks.

DO NOT:
  ✗ Register any of the example domains shown
  ✗ Use these techniques for unauthorized access or fraud
  ✗ Distribute this tool with malicious intent

The author takes no responsibility for misuse of information presented here.
This platform is built in the spirit of responsible disclosure and public
security education.
```

---

## 📜 License

```
MIT License — Free to use, modify, and distribute with attribution.
© 2025 Kiran Kumar K — kirankumark-sec
```

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,30:003366,70:00ff88,100:0d1117&height=120&section=footer&animation=fadeIn" width="100%"/>

**⭐ If this helped you learn something — star the repo and share it with your team.**

`Offensive mind. Defensive discipline.`

</div>
