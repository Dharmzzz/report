# 📖 3D Realistic PDF Flipbook & Report Reader

> A turn-key, high-performance in-browser **3D Digital Flipbook** that turns standard PDF documents into realistic, tactile hardcover books with **natural page curls**, **antique parchment textures**, **zoom & pan**, and **multi-report switching**.

---

## 🌟 What Is This? (Zero Coding Knowledge Needed)

Imagine handing your website visitors a real physical book instead of a boring scrollable PDF:
- **Realistic Page Turning**: Drag the corner of a page with your mouse or finger, or click the buttons to see it curl and turn in realistic 3D space with authentic shadows.
- **Antique Hardcover Binding**: Includes a gilded filigree outer frame, gold-embossed typography, spine creases, and an antique medallion seal.
- **Aged Paper & Burnt Edges**: Inner pages have warm parchment aging, spine depth shadows, and subtle scorched edge patterns.
- **High-Definition Reading**: Renders PDF text and charts razor-sharp on retina and 4K screens using high-DPI canvas scaling.
- **Multi-Publication Switcher**: Includes a dropdown selector containing **10 complete Rajagiri Annual Reports (2014 to 2024)**.
- **Full Zoom & Pan**: Zoom in up to 250% to read small print, and drag to pan smoothly around the page.

---

## 🚀 Quick Start Guide (Run It In 60 Seconds)

Because this project runs in standard web browsers, you can start it immediately with any of the following 3 easy methods:

### Method 1: Using Python (Built into Windows, Mac, and Linux!)
1. Open your terminal or Command Prompt.
2. Navigate to this folder:
   ```bash
   cd "path/to/report"
   ```
3. Type:
   ```bash
   python -m http.server 3000
   ```
4. Open your browser and go to: **`http://localhost:3000`**. Done!

---

### Method 2: Using Node.js / npm
1. Open your terminal in this folder.
2. Type:
   ```bash
   npm start
   ```
3. Open the link shown in your browser. Done!

---

### Method 3: Using VS Code Live Server
1. Open this folder in **VS Code**.
2. Right-click on **`index.html`** and select **"Open with Live Server"**. Done!

> 💡 **Why a local server?** Modern web browsers block PDFs from loading over `file:///` URLs due to local security (CORS) rules. Running a simple local server allows `PDF.js` to parse your PDFs smoothly.

---

## 🎬 Key Features Explained Simply

| Feature | What It Does In Plain Words |
| :--- | :--- |
| **No Manual Image Conversion** | You don't need to convert PDF pages into JPGs or PNGs! You simply drop in a `.pdf` file, and the browser automatically renders every page into a crisp image on the fly. |
| **Realistic 3D Page Physics** | Powered by **StPageFlip**, pages bend, cast natural drop shadows, and show interactive dog-ear corners when you hover over them. |
| **Vintage Hardcover Design** | Generates an authentic embossed front cover and back cover with your organization's name, crest, and motto. |
| **Zoom & Drag-to-Pan** | Use the `+` and `-` buttons to zoom in on complex tables or fine print, then click and drag anywhere to pan around the page. |
| **Multi-Publication Dropdown** | Switch between different annual reports, magazines, or books from a single dropdown without reloading the page. |
| **100% Mobile Responsive** | Displays as a full 2-page open book on laptops and desktops, and automatically switches to single-page portrait reading on smartphones. |

---

## 📦 Required Dependencies & What Each One Does

1. **`pdf.js` & `pdf.worker.js` (Mozilla)**
   - *What it is*: The world-standard open-source PDF parsing engine created by Mozilla (the creators of Firefox).
   - *Why we use it*: Reads binary `.pdf` files directly in the browser and renders each page onto an HTML5 `<canvas>` element at 1.5x retina scaling.

2. **`StPageFlip` (`page-flip.browser.js`)**
   - *What it is*: A lightweight 3D canvas/HTML book flip physics engine.
   - *Why we use it*: Computes real-time page deformation, corner dragging, spine depth shadows, and realistic turning curves.

3. **`Bootstrap Icons`**
   - *What it is*: Clean, lightweight SVG vector icons.
   - *Why we use it*: Powers the previous, next, first, last, zoom-in, zoom-out, and reset-zoom buttons.

4. **Google Fonts (`Cinzel` & `Playfair Display`)**
   - *What it is*: High-class serif and display typography.
   - *Why we use it*: Provides the authentic gold-leaf lettering on the book's hardcover and flyleaf pages.

---

## 🎨 How to Add Your Own PDFs

Adding your own annual report, booklet, or magazine is as easy as 1-2-3:

1. **Copy your PDF** into the `pdfs/` folder (e.g. `pdfs/my-new-report.pdf`).
2. **Open `index.html`** and add your file to the `<select id="pdf-selector">` list:
   ```html
   <select id="pdf-selector">
     <option value="pdfs/my-new-report.pdf">My New Annual Report 2025</option>
     <!-- other options -->
   </select>
   ```
3. Refresh your browser — your new PDF will immediately render as a 3D flipbook!

---

## 📁 Project Structure

```
report/
├── README.md                      # This guide
├── INTEGRATION_PROMPT.md          # Copy-paste AI prompt for integrating into any project
├── package.json                   # npm start script
├── index.html                     # Standalone HTML application
├── .gitignore                     # Git ignore rules
│
├── css/
│   └── flipbook.css               # Complete vintage styling, burnt edges & zoom layout
├── js/
│   └── flipbook.js                # PDF.js decoder & StPageFlip 3D physics controller
├── assets/
│   └── logorajagiri.png           # Emblem / crest logo used on front & back covers
└── pdfs/                          # 10 complete Rajagiri OYSTER Annual Reports (2014-2024)
    ├── Annual Report 2014-15-OYSTER.pdf
    ├── Annual Report 2015-16-OYSTER.pdf
    ├── Annual Report 2016-17-OYSTER.pdf
    ├── Annual Report 2017-18-OYSTER.pdf
    ├── Annual Report 2018-19-OYSTER.pdf
    ├── Annual Report 2019-20-OYSTER.pdf
    ├── Annual Report 2020-21.pdf
    ├── Annual Report 2021-22.pdf
    ├── Annual Report 2022-23.pdf
    └── ANNUAL REPORT 2023-24.pdf
```

---

## 🤖 Integrating Into Another Project with AI

Want to add this exact 3D flipbook reader into your Next.js, Django, Laravel, Vue, or WordPress project?
Open **[`INTEGRATION_PROMPT.md`](./INTEGRATION_PROMPT.md)**, copy the prompt, and paste it to **ChatGPT**, **Claude**, **Cursor**, or **Gemini**!

---

## 📜 License & Credits

- Created for **Rajagiri College of Social Sciences (RCSS)** & **OYSTER Alumni Association**.
- Released under the **MIT License**. Free to use, customize, and integrate into any personal or commercial project.
