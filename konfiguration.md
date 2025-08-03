# SAP MM – Configuration Overview (Demo Project)

This file outlines the key configuration and master data elements used in the SAP MM procurement process demonstrated in this repository.

---

## 🔧 1. Scope of the Demo

This project demonstrates a simplified procurement process in SAP MM using standard GUI transactions. It covers the following steps:

- ME51N – Purchase Requisition
- ME21N – Purchase Order
- MIGO – Goods Receipt
- MIRO – Invoice Verification

The demo was created in a non-productive SAP environment for educational and portfolio purposes.

---

## 🏢 2. Organizational Structure

| Element                | Value     |
|------------------------|-----------|
| Client (Mandant)       | 800       |
| Company Code           | US00      |
| Plant                  | MI00      |
| Storage Location       | MI00      |
| Purchasing Org         | US00      |
| Purchasing Group       | N00       |

---

## 📦 3. Master Data

### Vendor

- Created via transaction **XK01**
- Name: Mid-West Supply  
- Account Group: KRED  
- Reconciliation Account: 300000  
- Payment Terms: 0001  

### Material

- Created via transaction **MM01**
- Material Number: CHLK1XXX (custom demo format)
- Type: ROH (Raw Material)
- Base Unit: PC
- Valuation Class: 3000  
- Standard Price: 10 USD

### Info Record

- Created via transaction **ME11**
- Vendor + Material combination
- Standard Quantity: 1  
- Net Price: 30 USD

---

## 🧾 4. Transaction Settings

### Purchase Requisition (ME51N)

- Document Type: NB  
- Account Assignment: K (Cost Center)  
- Cost Center: NAPC1000

### Purchase Order (ME21N)

- Document Type: NB  
- Source of Supply manually selected  
- Reference to PR

### Goods Receipt (MIGO)

- Movement Type: 101  
- Reference Document: PO  
- Stock updated at plant MI00

### Invoice Verification (MIRO)

- Reference to PO  
- 3-Way Match active  
- Invoice posted only after GR

---

## ⚙️ 5. Simplifications

This demo uses the following simplifications:

- No release strategy for PO or PR
- No batch management or serial numbers
- No freight or additional conditions
- No output messages or printing
- No vendor evaluation or scheduling agreements

---

## 📌 Notes

- All screenshots, data, and documents were generated in a sandbox environment.
- The process flow is aligned with SAP standard best practices.
- The content is intended for personal learning and job applications only.

---

_Last updated: August 2025_
