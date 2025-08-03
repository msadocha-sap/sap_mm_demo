# Step-by-Step Guide – SAP MM Procurement (Demo)

This file documents a full example of the standard SAP MM procurement process using the GUI, based on the demo data and screenshots from this repository.

---

## 1. Create Purchase Requisition

**Transaction:** ME51N

- Document Type: NB
- Material: CHLK1025 – Chain Lock 025
- Quantity: 100 PC
- Plant: DC Miami (MI00)
- Storage Location: Miscellaneous (MI00)
- Purchasing Group: N00
- Delivery Date: 09.08.2025

✅ Purchase requisition was created successfully.  
📷 Screenshot: `screens/pr_me51n.png`

---

## 2. Display Purchase Requisition (optional)

**Transaction:** ME53N / ME52N

- Used to verify or change the PR before PO creation

📷 Screenshot: `screens/po_me21n.png` (overview context)

---

## 3. Post Goods Receipt

**Transaction:** MIGO

- Transaction Type: Goods Receipt
- Reference Document: Purchase Order
- Posting Date: 03.08.2025
- Movement Type: 101
- Stock Type: Unrestricted-Use
- Plant: DC Miami (MI00)
- Storage Location: Miscellaneous (MI00)
- Quantity: 100 PC

✅ Material document was posted.  
📷 Screenshot: `screens/gr_migo.png`

---

## 4. Post Invoice

**Transaction:** MIRO

- Transaction Type: Invoice
- Reference PO: 4500002792
- Invoice Date: 03.08.2025
- Posting Date: 03.08.2025
- Amount: 10 000,00 USD
- Reference: INVOICE NR 01
- Tax Code: XI (Input Tax)
- Vendor: Fun n the Sun Seats n Bars

✅ Invoice was entered and balanced.  
📷 Screenshot: `screens/ir_miro.png`

---

## ✅ Final Process Overview

**End-to-end process:**
1. ME51N → Purchase Requisition  
2. ME21N → Purchase Order  
3. MIGO → Goods Receipt  
4. MIRO → Invoice Receipt

This scenario demonstrates a complete 3-way match cycle in SAP MM using basic master data and transactions.

---

_Last updated: August 2025_
