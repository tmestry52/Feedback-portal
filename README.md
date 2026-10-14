# 📊 Feedback Collation & Caller Analytics Portal

A complete, production-ready web application for collecting daily calling feedback from managers across India, detecting and highlighting duplicate entries, tracking caller-wise PTP and hit-rates, and consolidating files into a single master Excel report for Central Admin.

---

## 🚀 Key Features

1. **🔐 Role-Based Access Control**:
   - **Managers**: Can only upload their branch/team's data, view their callers' metrics, and inspect their double entries.
   - **Central Admin**: Has full national access, multi-manager filtering, master collation download, and user management.

2. **📄 Standardized Excel Template**:
   - One-click blank template download (`Feedback_File_Format.xlsx`).
   - Contains all mandatory 9 columns: `CUSTOMER ID`, `CUSTOMER NAME`, `CONTACT NO`, `CALLING DATE`, `FEEDBACK`, `DESP CODE`, `PORTFOLIO`, `MANAGER NAME`, `CALLER NAME`.
   - Includes approved disposition codes (`PTP`, `RNR`, `CB`, `NI`, `WN`, `PAID`).

3. **⚠️ Automated Double Entry Highlighting & Prevention**:
   - **Condition**: Same Customer ID/Contact + Same Calling Date + Same Disposition Code + Same Feedback.
   - Rows matching this condition are highlighted in **Red** with `⚠️ Double Entry (Call 1/2)` and `(Call 2/2)` badges and Excel row numbers.
   - **`📥 Download Double Entry File (.xlsx)`** button allows managers to immediately export duplicate records to share with callers.
   - **"Exclude Double Entries"** toggle ensures calling stats and PTP hit rates are 100% accurate.

4. **📈 Caller Performance & Daily PTP Analytics**:
   - Total Calls per caller.
   - Today's PTPs generated and conversion % per caller.
   - Daily disposition share (PTP, RNR, Call Back, Not Interested).

5. **⬇️ Master Collation Center (Admin Exclusive)**:
   - Consolidates all uploaded manager Excel files into one unified Master Excel report with 1 click.
   - Filter by Calling Date range, Manager, and Portfolio.

---

## 🔑 Login Credentials

| Role | Username | Password | Access Level |
| :--- | :--- | :--- | :--- |
| **Central Admin** | `ADMIN` | `Tejas@123` | Full National Master Access & User Management |
| **Manager ** | `AMBUJ T` | `Ambuj@123` |  Calling & Upload Access |
| **Manager ** | `SHRAVANTHI P` | `Shravanthi@123` |  Calling & Upload Access |
| **Manager ** | `OMKAR S` | `Omkar@123` |  Calling & Upload Access |
| **Manager ** | `ADITI G` | `Aditi@123` |  Calling & Upload Access |
| **Manager ** | `SMITA J` | `Smita@123` |  Calling & Upload Access |
| **Manager ** | `SHWETA S` | `Shweta@123` |  Calling & Upload Access |

*(Admin can add or delete manager accounts anytime from the "Manage Users" tab)*

---

## 🌐 How to Host on GitHub (GitHub Pages)

Because this portal is built with clean, client-side web technologies and standard SheetJS + Chart.js, it can be hosted for **free on GitHub Pages** in 2 minutes:

### Step 1: Create a GitHub Repository
1. Go to [github.com](https://github.com) and log in.
2. Click **New Repository**.
3. Name it: `feedback-collation-portal` (Set to **Public** or **Private**).

### Step 2: Upload Files
Upload all files in this folder to the repository:
- `index.html` *(Main portal)*
- `xlsx.full.min.js` *(Excel engine)*
- `Feedback File Format.xlsx` *(Template file)*
- `README.md`

### Step 3: Enable GitHub Pages
1. In your GitHub repository, click **Settings** (⚙️).
2. On the left sidebar, click **Pages**.
3. Under **Branch**, select `main` (or `master`), folder `/ (root)`, and click **Save**.
4. Within 1 minute, GitHub will give you a live URL:
   `https://<your-username>.github.io/feedback-collation-portal/`

👉 **Any manager can now open this link on their mobile or laptop and log in with their credentials!**

---

## 💻 Running Locally (Offline Mode)

If you prefer to run locally on your office network:
1. Double-click `Start_Portal.bat`.
2. The portal will automatically start the background server and open `index.html` in your default browser at `http://localhost:3000/`.
