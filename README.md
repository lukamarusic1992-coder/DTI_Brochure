# Airocle DTI Brochure System

**Direct-to-Industry Sales Brochure** — Problem-specific landing pages and print-ready A4 inserts for Airocle's sales team.

## 🎯 What This Is

Instead of one generic brochure, each prospect gets a **custom landing page** that speaks directly to their specific problem. Each page comes with a **matching A4 double-sided insert** for print or email.

**5 Industry Problems:**
1. 🔴 **Heat Load & Thermal Discomfort** ✅ Complete
2. 💨 **Air Quality & Fumes** (Coming soon)
3. 💧 **Condensation Control** (Coming soon)
4. ⚙️ **End-of-Life Replacement** (Coming soon)
5. 🔥 **Smoke Management Compliance** (Coming soon)

---

## 📁 Project Structure

```
dtibrochure/
├── index.html                   # Home page with problem navigation
├── css/
│   └── style.css               # Shared styles, colors, typography
├── pages/
│   ├── heat.html               # Heat landing page
│   └── ...                      # Other problem pages
├── inserts/
│   ├── heat-insert.html        # Heat A4 double-sided one-pager
│   └── ...                      # Other inserts
└── assets/
    ├── images/
    │   ├── heat/               # Heat problem images
    │   └── ...
    └── icons/                  # SVG icons
```

---

## 🚀 Getting Started

### View Online
- **Home:** https://dtibrochure-nu.vercel.app/
- **Heat Landing Page:** https://dtibrochure-nu.vercel.app/pages/heat.html
- **Heat A4 Insert:** https://dtibrochure-nu.vercel.app/inserts/heat-insert.html

### Local Development
```bash
# Clone the repo
git clone <your-repo-url>
cd dtibrochure

# Open index.html in a browser
open index.html

# Or run a local server
python -m http.server 8000
# Visit http://localhost:8000
```

---

## 🎨 Design System

### Colors
All colors are defined in `css/style.css` using CSS variables:

```css
:root {
    /* Brand */
    --color-sky-blue: #266ED9;
    --color-navy: #002D41;
    
    /* Problem Accents */
    --color-heat: #D32F2F;           /* Red */
    --color-fumes: #7B2CBF;          /* Purple */
    --color-condensation: #00838F;   /* Teal */
    --color-endoflife: #2E7D32;      /* Green */
    --color-smoke: #C62828;          /* Dark Red */
}
```

### Typography
- **Sans Serif:** System font stack (Segoe UI, Roboto, etc.)
- **Hierarchy:** h1 (48px), h2 (32px), h3 (18px), p (16px)
- **Weights:** 600 (bold), 700 (extra bold)

### Spacing
Consistent spacing scale:
- `--spacing-xs: 4px`
- `--spacing-sm: 8px`
- `--spacing-md: 12px`
- `--spacing-lg: 20px`
- `--spacing-xl: 30px`
- `--spacing-2xl: 40px`

---

## 📄 Landing Page Structure

Each landing page follows the same modular structure:

1. **Hero Section** — Problem headline + CTA
2. **Hero Image** — Facility/industry photo
3. **Problem Section** — 4 problem boxes (2x2 grid)
4. **Solution Section** — 3-step process
5. **Thermal/Performance Section** — Before/after visuals + benefits
6. **Case Study Section** — Featured project
7. **Key Benefits Section** — 3 big numbers
8. **Final CTA Section** — Dark background, clear call-to-action
9. **Footer** — Contact details

---

## 📋 A4 Insert Structure

Each A4 one-pager is designed for print (double-sided):

### **Front Page:**
- Hero band (colored background) with headline + CTA
- Large hero image (40% of page)
- 4 problem boxes in 2x2 grid

### **Back Page:**
- How it Works (3-step process)
- Featured Project (prominent bordered box)
- Benefits (4 items in 2-column layout)
- Key Numbers (3 big results)
- Footer

**Dimensions:** 210mm × 297mm (A4 standard)  
**Print:** Opens in browser, export to PDF or print directly

---

## 🔧 How to Add a New Problem

### Step 1: Create the Landing Page

Copy `pages/heat.html` and update:
- Change `--color-heat` references to your problem's color
- Update headline (`.hero h1`)
- Update the 4 problem boxes
- Update 3-step process
- Update case study
- Update all copy/content

### Step 2: Create the A4 Insert

Copy `inserts/heat-insert.html` and update:
- Same color changes as above
- Condensed copy for print format
- Case study details

### Step 3: Add to Navigation

Update `index.html`:
- Add a new problem link card in `.problems-nav`
- Link to the new landing page and insert

### Step 4: Add Assets

Create folders for your images:
```
assets/images/[problem-name]/
├── hero.jpg
├── before.jpg
├── after.jpg
├── case-study.jpg
└── ...
```

---

## 🖼️ Image Guidelines

### Landing Page
- **Hero Image:** 1200px wide, 400px tall (or 16:9 ratio)
- **Case Study Image:** 600px × 400px
- **Before/After Images:** 400px × 300px (landscape)

### A4 Insert
- **Hero Image:** 170mm wide, ~100mm tall
- **All images:** High quality, industrial/facility focused
- **Format:** JPG (web optimized) or PNG

---

## 📤 Deployment

### Auto-Deploy (Recommended)
Push to GitHub → Vercel auto-deploys

```bash
git add .
git commit -m "Add [problem-name] landing page and A4 insert"
git push origin main
```

### Manual Deploy
Visit https://vercel.com → Link your GitHub repo → Deploy

---

## ✅ Checklist for New Problem

- [ ] Landing page created (`pages/[problem].html`)
- [ ] A4 insert created (`inserts/[problem]-insert.html`)
- [ ] Images added to `assets/images/[problem]/`
- [ ] Color variable added to `css/style.css`
- [ ] Problem added to `index.html` navigation
- [ ] All copy proofread and accurate
- [ ] All CTAs set to correct contact method
- [ ] Tested on desktop and mobile
- [ ] Tested print preview of A4 insert
- [ ] Pushed to GitHub and deployed

---

## 🎓 Tips for Sales Team

### Using Landing Pages
1. Identify prospect's **specific problem** (heat, fumes, condensation, etc.)
2. Send them the **matching landing page** — not the homepage
3. Say something like: *"I found this — looks like it addresses exactly what you mentioned"*
4. Follow up: *"Did you have a chance to look at that? I'd love to walk you through a quick assessment"*

### Using A4 Inserts
1. **Print** for face-to-face meetings (leave behind)
2. **Email** as PDF attachment with personalized message
3. **Folder** as insert in a physical sales folder/pocket
4. **Social** as downloadable resource on LinkedIn

---

## 📞 Support

For questions or to request a new problem page:
- Email: hello@airocle.com.au
- Website: www.airocle.com.au

---

## 📝 Version History

**v1.0** — 2026-11-11
- ✅ Heat problem complete (landing page + A4 insert)
- 🚀 System ready for other 4 problems
- Deployed on Vercel

---

**Built with:** HTML5, CSS3, responsive design  
**Deployed on:** Vercel  
**Updated:** 2026-11-11
