# MoizHR — Enterprise Employee Management System

<div align="center">
<img width="1918" height="906" alt="P1" src="https://github.com/user-attachments/assets/087c9d9f-59e0-4574-9f3d-ca45f740de42" />
  
<img width="1916" height="892" alt="P2" src="https://github.com/user-attachments/assets/3645a2a7-30d2-4432-8198-458ce778019f" />

<img width="1918" height="890" alt="p3" src="https://github.com/user-attachments/assets/5ff938f2-67b0-49c9-91d1-03de2fa85193" />

<img width="1917" height="911" alt="P4" src="https://github.com/user-attachments/assets/084ca41f-5dd8-4904-98c6-9720e3df4991" />

<img width="1918" height="887" alt="P5" src="https://github.com/user-attachments/assets/89638b91-ce3d-464b-b819-e5ca074d8d66" />


**A fully client-side, zero-dependency HR management system built with pure HTML, CSS, and JavaScript.**  
No backend. No database server. No installation required.

[🚀 Live Demo](#) · [📹 Video Walkthrough](VIDEO.md) · [🐛 Report Bug](../../issues) · [✨ Request Feature](../../issues)


---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Screenshots](#-screenshots)
- [Getting Started](#-getting-started)
- [Usage Guide](#-usage-guide)
- [Project Structure](#-project-structure)
- [CSV Import Format](#-csv-import-format)
- [Browser Support](#-browser-support)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## 🌟 Overview

**MoizHR** is a production-grade, single-file Employee Management System designed for small to medium organizations. It runs entirely in the browser with no server, no backend, and no installation — just open the HTML file and start managing your workforce.

All data is persisted locally in the browser's `localStorage`, making it portable and private by default.

> 📹 **Want to see it in action?** Check out the [Video Demo](VIDEO.md).

---

## ✨ Features

### 📊 Dashboard & Analytics
- Real-time organizational statistics (Total Headcount, Active Staff, Average Salary, On Leave)
- **Department Distribution** — Interactive doughnut chart
- **Hiring Activity** — Year-over-year bar chart
- Instant stats refresh whenever data changes

### 👥 Employee Directory
- Full searchable, filterable employee table
- **Multi-column sorting** — Click any column header to sort ascending/descending
- **Pagination** — Configurable page size (5 / 10 / 25 / 50 per page)
- Smart page range with ellipsis for large datasets

### 👤 Employee Profile View
- Click the 👁 eye icon on any row to open a clean read-only profile modal
- Displays all details: name, position, salary, email, phone, join date, rating, status
- Quick **Edit** and **Delete** actions directly from the modal

### ➕ Employee Onboarding Form
- Add new employees with a fully validated multi-field form
- Inline field-level error messages (not just generic alerts)
- Salary guardrails: min $1,000 — max $5,000,000
- Auto-generated unique System ID per employee
- Edit existing profiles seamlessly with pre-filled form

### 📥 CSV Import
- Drag-and-drop or file-browse CSV import
- Automatic duplicate detection by email
- Downloadable CSV template for easy onboarding
- Import feedback showing records added vs. skipped

### 📤 CSV Export
- One-click export of the full employee dataset
- Timestamped filename (`MoizHR_Export_YYYY-MM-DD.csv`)

### 🌗 Dark / Light Mode
- Smooth theme toggle with full CSS variable support
- Theme preference persisted across browser sessions

### 📱 Fully Responsive
- Mobile-friendly sidebar with overlay and hamburger toggle
- Adapts cleanly from desktop to tablet to mobile

---

## 🛠 Tech Stack

| Category | Technology | Purpose |
|---|---|---|
| **Markup** | HTML5 | Structure, forms, semantic layout |
| **Styling** | CSS3 | Custom properties, Flexbox, Grid, animations |
| **Logic** | Vanilla JavaScript (ES6+) | All app logic, DOM, data management |
| **UI Framework** | Bootstrap 5.3 | Responsive grid, utility classes |
| **Icons** | Bootstrap Icons 1.10 | All UI icons |
| **Charts** | Chart.js | Dashboard doughnut & bar charts |
| **Fonts** | Google Fonts (DM Sans, DM Mono) | Typography |
| **Storage** | Browser LocalStorage | Client-side data persistence |
| **File APIs** | FileReader API, Blob API | CSV import and export |
| **Drag & Drop** | HTML5 Drag and Drop API | CSV drag-and-drop zone |

### Design Patterns Used
- **SPA (Single Page Application)** — View toggling without page reloads
- **CRUD** — Full Create, Read, Update, Delete for employee records
- **CSS Theming** — Dark/light mode via `data-theme` and CSS custom properties
- **Client-side pagination** — With smart ellipsis page range
- **Client-side sort & filter** — Real-time multi-criteria filtering

---

## 🚀 Getting Started

### Option 1 — Direct Open (Quickest)

1. Download `index.html`
2. Double-click it to open in any modern browser
3. That's it — no setup needed!

### Option 2 — GitHub Pages (Live URL)

1. Fork this repository
2. Go to **Settings → Pages**
3. Set source to `main` branch / root
4. Your app will be live at `https://YOUR-USERNAME.github.io/MoizHR-Employee-Management/`

### Option 3 — Local Server (Optional)

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .
```

Then open `http://localhost:8000` in your browser.

---

## 📖 Usage Guide

### Adding an Employee
1. Click **"Hire Employee"** on the Dashboard or **"Add New"** in the Directory
2. Fill in the required fields (marked with `*`)
3. Click **"Save Profile"** — the employee is instantly added

### Editing an Employee
- Click the ✏️ **pencil icon** in the Directory table, or
- Open the 👁 **Profile View** and click **"Edit Profile"**

### Deleting an Employee
- Click the 🗑️ **trash icon** in the Directory table, or
- Open the Profile View and click **"Delete"**
- A confirmation prompt will appear before deletion

### Importing Employees via CSV
1. Go to **Directory → Import CSV**
2. Drag-and-drop your CSV file or click to browse
3. Download the **template** if you're unsure of the format
4. Duplicate emails are automatically skipped

### Exporting Data
- Click **"Export CSV"** in the Directory toolbar
- A formatted CSV file downloads instantly

### Switching Themes
- Click **"Dark Mode / Light Mode"** at the bottom of the sidebar

---

## 📁 Project Structure

```
MoizHR-Employee-Management/
│
├── index.html          # Complete application (single file)
├── README.md           # Project documentation
├── VIDEO.md            # Video demo and walkthrough
└── LICENSE             # MIT License
```

> This is intentionally a **single-file application**. All HTML, CSS, and JavaScript live in `index.html` for maximum portability — no build tools, no bundlers, no dependencies to install.

---

## 📄 CSV Import Format

When importing employees, your CSV must include at minimum a `Name` and `Email` column.

```csv
Name,Email,Phone,Department,Position,Salary,Join Date,Rating,Status
Jane Doe,jane@example.com,555-000-1234,Engineering,Software Engineer,90000,2025-01-15,4,Active
John Smith,john@example.com,555-999-8888,Design,UI Designer,85000,2024-06-01,3,Active
```

**Accepted Departments:** `Engineering`, `Product`, `Design`, `HR`, `Marketing`, `Sales`, `Finance`

**Accepted Statuses:** `Active`, `Inactive`

**Rating:** Integer from `0` (unrated) to `5`

> 💡 Download the built-in template from the Import modal to get started quickly.

---

## 🌐 Browser Support

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Opera 76+ | ✅ Full |
| IE 11 | ❌ Not supported |

---

## 🗺 Roadmap

- [ ] Employee photo upload support
- [ ] Department management (add/rename/delete)
- [ ] Leave request tracking
- [ ] Salary history timeline per employee
- [ ] Print-friendly employee profile PDF
- [ ] Role-based access control (Admin / HR / Viewer)
- [ ] Cloud sync via Firebase or Supabase
- [ ] Multi-language (i18n) support

---

## 🤝 Contributing

Contributions are welcome! Here's how to get involved:

1. **Fork** the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes to `index.html`
4. **Commit** your changes: `git commit -m "Add: your feature description"`
5. **Push** to your branch: `git push origin feature/your-feature-name`
6. Open a **Pull Request**

Please keep code clean, well-commented, and consistent with the existing style.

---

## 📜 License

This project is licensed under the **MIT License** — you are free to use, modify, and distribute it for personal or commercial projects.

See the [LICENSE](LICENSE) file for full details.

---

## 👨‍💻 Author

**Moiz**

> Built with ❤️ using pure HTML, CSS, and JavaScript — no frameworks, no fuss.

---

<div align="center">

⭐ **If you found this project useful, please give it a star!** ⭐

</div>
