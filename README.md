# Price Dashboard

A premium, glassmorphic dark-themed online dashboard to monitor 9 key price and inflation indicators for Malaysia. The dashboard utilizes live data from Google Drive (via Google Sheets public CSV export) and displays trends using micro-animated sparklines and interactive Chart.js line charts.

## 📊 Dashboard Structure (9 Indicators Grid)

The grid layout forms a perfect 3x3 matrix:

*   **Row 1:** CPI - Monthly • CPI - Quarterly • CPI - Annual
*   **Row 2:** PPI - Monthly • PPI - Quarterly • PPI - Annual
*   **Row 3:** SPPI - Quarterly • SPPI - Annual • Overnight Policy Rate (OPR)

---

## ⚙️ Google Sheets Live Sync Setup

The dashboard is hardcoded to sync with the spreadsheet:
`https://docs.google.com/spreadsheets/d/1bTfW9RIot6i44Pg19xkAuYvzODZWoYZQibIkkryX0UQ/edit?usp=sharing`

### Supported Sheet Tab Names

Your Google Sheet must contain separate **sheet tabs** for each indicator:

| Sheet Tab Name | Short Code | Indicator Display Name |
| :--- | :--- | :--- |
| `cpi_monthly` | CPI M | CPI - Monthly |
| `cpi_quarterly` | CPI Q | CPI - Quarterly |
| `cpi_annual` | CPI A | CPI - Annual |
| `ppi_monthly` | PPI M | PPI - Monthly |
| `ppi_quarterly` | PPI Q | PPI - Quarterly |
| `ppi_annual` | PPI A | PPI - Annual |
| `sppi_quarter` | SPPI Q | SPPI - Quarterly |
| `sppi_annual` | SPPI A | SPPI - Annual |
| `opr` | OPR | Overnight Policy Rate (OPR) |

> **Note:** If a tab name is missing from your sheet, the dashboard will automatically load realistic mock data for that indicator instead. This allows you to build out your spreadsheet one tab at a time!

### Format Your Tab Columns

In each tab, create exactly two columns: **`date`** and **`value`**.

#### Example Tab (`cpi_monthly`):
| date | value |
| :--- | :--- |
| `2025-06` | `2.0` |
| `2025-07` | `2.1` |
| `2025-08` | `2.0` |

#### Date Formats to Use:
- **Monthly Indicators:** Use `YYYY-MM` format (e.g., `2026-05`).
- **Quarterly Indicators:** Use `YYYY-QX` format (e.g., `2026-Q2`).
- **Annual Indicators:** Use standard `YYYY` format (e.g., `2025`).

---

## 🛠️ Verification & Development

To access the dashboard:
1. Ensure the Python local server is running.
2. Navigate to `http://localhost:8001` in your browser.
3. Click the **Refresh** button in the header to pull latest changes from the Google Sheet.
