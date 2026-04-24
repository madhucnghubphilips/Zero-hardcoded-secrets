# Zero-hardcoded-secrets
Standardized dummy credential framework as a preventive and scalable solution to eliminate hardcoded secret risks at the source

![platform](https://img.shields.io/badge/PCI-DSS-blue)
![platform](https://img.shields.io/badge/Payment-Gateway-purple)
![](https://img.shields.io/badge/Threat%20Model-STRIDE,%20IriusRisk-yellow)
![platform](https://img.shields.io/badge/Proxy-OWASP%20ZAP,%20Burpsuite-green)
![platform](https://img.shields.io/badge/SAST-Fortify,%20Coverity,%20BlackDuck,%20GitSec,%20Checkov-orange)
 

<!-- GIF -->
<img align="center" height="400" width="800" src="https://github.com/madhucnghubphilips/Zero-hardcoded-secrets/blob/main/Hardcoded%20Secrets.png"/>


# Eliminating Hardcoded Secrets in Source Code  
## A Standardized Dummy Credential Framework

---

## 📄 Abstract
Hardcoded secrets remain a pervasive and high-impact vulnerability in modern software development practices. Despite widespread adoption of automated detection mechanisms such as Static Application Security Testing (SAST) and secret scanning tools, organizations continue to face recurring risks due to credential exposure, lack of lifecycle management, and persistent false positives. :contentReference[oaicite:0]{index=0}  

This paper presents a **standardized dummy credential framework** as a preventive and scalable solution to eliminate hardcoded secret risks at the source. By enforcing consistent dummy credential patterns across all non-production artifacts, organizations can:  

- Clearly differentiate between sensitive and non-sensitive data  
- Reduce false positive recurrence  
- Improve the efficiency of security validation processes  

This approach aligns with secure software development practices and supports compliance with standards such as **ISO/IEC 27001** and guidance from **NIST**.  

---

## 🚀 Introduction
The rapid evolution of **DevSecOps** practices has significantly improved software delivery speed and collaboration. However, it has also amplified the risk of sensitive data exposure within source code repositories. :contentReference[oaicite:1]{index=1}  

Hardcoded credentials—such as API keys, tokens, and passwords—are frequently introduced during development and testing phases and often persist unnoticed across the software lifecycle.

These credentials propagate across:
- Version control systems  
- CI/CD pipelines  
- Distributed environments  

…creating a systemic security weakness.

---

## ⚠️ The Core Problem

In modern development and testing environments, dummy or inactive credentials are often required to simulate real-world scenarios. However:

- Secret scanning tools frequently flag these as real exposures  
- High volumes of **false positives** are generated  
- Developers must repeatedly validate the same findings  

### 🔁 Tooling Challenge
Even though tools like:
- GitHub Advanced Security  
- git-secrets  

allow false positive classification, these:
- Are **tool-specific**
- Lack **portability across tools**
- Do not persist across tool upgrades or migrations  

👉 Result:
- Repeated validation cycles  
- Increased developer fatigue  
- Reduced productivity  
- Alert fatigue  

---

## 🔍 Example: Ambiguous Credentials

```javascript
// auth.test.js
const ClientId = "3f9a2c44-8b7d-4e1a-9c2f-6d8e5a1b2c3d";
const ClientSecret = "Vh7$kL9pQ2xZrT6mN8sW4yB!cD0eF1gH"; 

test("should return mock token", () => {
  expect(ClientSecret).toBeDefined();
});




<!-- Header Section -->
<h2 align="left"><font face="Arial">Payment security encompasses the systems, processes, and safeguards designed to protect financial transactions from unauthorized access, data breaches, and fraud. Whether for online or offline businesses, robust payment security is crucial for maintaining customer trust, preventing financial losses, and adhering to relevant regulations and industry standards.</font></h2>

<h2 align="left"><font face="Arial">The payment systems involves;</font></h2> 
Three computer systems are involved whenever a customer makes a card/online purchase online. <br>

**The merchant website** 
Contains the product catalogue and shopping cart. Always starts the process to collect the customer’s cardholder data when the customer asks to checkout. <br>

**The customer computer:**
Running a web browser such as Firefox, Chrome or Internet Explorer. <br>

**The payment service provider (PSP):**
is a third-party company that facilitates the processing of online payments for businesses. PSPs enable merchants to accept various payment methods, including credit cards, debit cards, bank transfers, digital wallets, and more, through a single platform. They handle the technical and security aspects of payment processing, allowing businesses to focus on their core operations. <br>

