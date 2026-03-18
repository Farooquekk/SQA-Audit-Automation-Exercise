
---

# Test Strategy: E-Commerce Platform Audit (Automation Exercise)

## 1. Introduction

This document outlines the strategic approach for the Manual Software Quality Assurance (SQA) and Security Audit of the [Automation Exercise](https://automationexercise.com/) platform. The goal is to ensure functional integrity, data consistency, and basic security resilience.

## 2. Scope of Testing

### **2.1 In-Scope (Functional)**

* **User Authentication:** Signup, Login, and Logout flows.
* **Product Management:** Search functionality, Category filtering, and Product Detail validation.
* **Cart & Checkout:** Add/Remove items, Quantity validation, and Payment gateway simulation.
* **Contact Us/Testimonials:** Form submissions and file uploads.

### **2.2 In-Scope (Security & Network)**

* **Traffic Analysis:** Using **Wireshark** to intercept and analyze HTTP/HTTPS traffic for plaintext data leaks.
* **Reconnaissance:** Using **NMAP** to identify open ports and service versions to assess the attack surface.
* **Input Validation:** Testing for common vulnerabilities like SQL Injection (SQLi) and Cross-Site Scripting (XSS) in search and login fields.

## 3. Test Methodology

I am adopting a **"Risk-Based Testing"** approach, prioritizing the checkout and login modules due to their high impact on business logic and security.

* **Black-Box Testing:** Testing the application interface without internal code access.
* **Boundary Value Analysis (BVA):** Specifically for product quantities and payment fields.
* **Exploratory Testing:** Unstructured testing to find edge cases in the user UI/UX.

## 4. Technical Stack & Tools

| Tool | Purpose |
| --- | --- |
| **Chrome DevTools** | DOM inspection, Console error monitoring, and Network throttling. |
| **Wireshark** | Packet sniffing to verify TLS encryption and session token handling. |
| **NMAP** | Network discovery and security auditing of the host. |
| **Draw.io / LucidChart** | Mapping **State Machine Diagrams** for the "Order Placement" logic. |
| **MS Excel / Google Sheets** | Test Case Management and Bug Tracking. |

## 5. Test Environment

* **Browser:** Google Chrome
* **OS:** Windows 10
* **Connection:** Stable Wi-Fi

## 6. Bug Severity & Priority Criteria

* **Critical (S1):** System crash, data loss, or security breach.
* **Major (S2):** Core functionality broken.
* **Minor (S3):** UI inconsistencies or spelling errors.

## 7. Deliverables

1. **Test Case Suite:** Detailed scenarios with Pass/Fail status.
2. **Bug Report:** Documented defects with reproduction steps.
3. **Security Audit Summary:** Insights from Wireshark/NMAP analysis.
4. **Logic Diagrams:** State Machine Diagram for the Checkout flow.

---
