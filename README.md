# 📦 Inventory Management App

Desktop inventory management system built for the **Formula SAE team at UNESP**, designed to run fully offline on a workshop computer with unstable network access.

The app replaced manual spreadsheets and improved how the team tracked parts, managed requests, and documented stock history during competition preparation.

---

## 🎯 Problem it solved

The Formula SAE workshop had unreliable internet connectivity, making cloud-based tools impractical. The team needed a fast, always-available solution to:

- Track available parts and materials
- Manage purchase requests with approval workflow
- Keep a complete audit log of stock changes
- Run on a fixed workshop PC without requiring Python installation

---

## ✨ Features

### 📊 Stock Overview
- View current inventory at a glance
- Search products by name
- Withdraw items with quantity validation

### 📝 Product Requests
- Submit requests with name, quantity, importance level, responsible person, and notes
- Auto-generated unique request ID per submission

### 📦 Request Tracking
- Filter requests by responsible person or request number
- Status update protected by password

### 🛠 Status Management
Requests flow through defined stages:
`Solicited → Under Analysis → Approved → Rejected → Delivered`

### ➕ Stock Management
- Add new products
- Restock existing items

### 🕓 Audit Log
- Complete history of all actions: additions, withdrawals, new registrations
- Filter by product, ID, or responsible person

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Language | Python |
| UI | Tkinter |
| Database | SQLite (local) |
| Distribution | Compiled to `.exe` — no Python required |

SQLite was chosen deliberately over a remote database to ensure zero-latency access and full offline operation in the workshop environment.

---

## 🚀 How to Run

**Option 1 — Run the executable (no setup needed):**

1. Download or clone this repository
2. Double-click `app_estoque.exe`

> ⚠️ Windows may show a security warning on first launch. Click **"More info" → "Run anyway"**. This is standard behavior for unsigned local apps.

**Option 2 — Run from source:**

```bash
git clone https://github.com/Lucasyuki01/Inventory-management-app.git
cd Inventory-management-app/Inventory_management
pip install -r requirements.txt
python main.py
```

---

## 💾 Data Storage

All data is stored in local `.csv` files in the same directory as the executable:

- `estoque.csv` — current stock
- `solicitacoes.csv` — requests log
- `historico.csv` — full audit trail

Keep all files in the same folder as `app_estoque.exe` for the app to work correctly.

---

## 🏎 Context

This project was built during my 3 years on the **Formula SAE UNESP** team, where I worked in the quality and continuous improvement area. Resource constraints were a constant challenge — this tool was one of several initiatives to improve our operational processes and documentation, contributing to consistent improvements in our competition ranking across three consecutive years.

---

## 👨‍💻 Author

**Lucas Yuki Nishimoto**
[github.com/Lucasyuki01](https://github.com/Lucasyuki01) · [lucasnishimoto.dev](https://lucasnishimoto.dev)
