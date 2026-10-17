# Sri Vijaya Nursing Home – Official Website Source

Production-ready, accessible, and SEO-optimized website for **Sri Vijaya Nursing Home**, operating two branches in **Kothagudem** and **Palvancha**, Bhadradri Kothagudem District, Telangana, India.

---

## 1. Project Overview & Directory Architecture

This website is built with clean, standards-compliant HTML5, modular CSS3, and lightweight Vanilla JavaScript. It requires zero compilation steps, bundlers, or third-party framework dependencies.

```
sri-vijaya-nursing-home/
├── 404.html                      # Branded 404 error page
├── about.html                    # About hospital, philosophy & standards
├── contact.html                  # Contact information, phone numbers & enquiry form
├── doctors.html                  # Medical staff profile (Dr. Vijaya Lakshmi)
├── index.html                    # Homepage / primary hospital hub
├── services.html                 # Comprehensive medical specialities & procedures
├── robots.txt                    # Search crawler indexing rules
├── sitemap.xml                   # XML sitemap for search engines
├── README.md                     # Documentation & operational checklist
├── assets/
│   ├── icons/                   # SVGs and UI iconography
│   └── images/
│       └── logo.png             # Official hospital logo
├── branches/
│   ├── kothagudem.html          # Kothagudem (Main Branch) dedicated page
│   └── palvancha.html           # Palvancha (Women's Healthcare) dedicated page
├── css/
│   └── style.css                # Master stylesheet with design tokens & responsive rules
└── js/
    └── script.js                # Mobile navigation, accordion, scroll reveal & validation
```

---

## 2. How to Run Locally

You can test and view this website locally using any standard web browser or local HTTP server:

### Option A: Direct File Execution (Simplest)
Double-click `index.html` or drag it into any modern web browser (Google Chrome, Microsoft Edge, Firefox, Safari).

### Option B: Python HTTP Server (Recommended)
Open a terminal in the `sri-vijaya-nursing-home` directory and execute:
```bash
# Python 3
python -m http.server 8000
```
Then visit `http://localhost:8000` in your browser.

### Option C: VS Code Live Server
1. Open the `sri-vijaya-nursing-home` folder in VS Code.
2. Install the **Live Server** extension (by Ritwick Dey).
3. Right-click `index.html` and choose **"Open with Live Server"**.

### Option D: Node.js `serve`
```bash
npx serve .
```

---

## 3. Deployment Instructions

This is a static site ready for immediate hosting on modern CDN platforms or traditional servers:

### A. Cloudflare Pages / Netlify / Vercel
1. Upload the project folder to GitHub / GitLab, or drag-and-drop the folder directly onto Cloudflare Pages / Netlify Drop (`app.netlify.com/drop`).
2. **Build command:** Leave empty (static site, no build step required).
3. **Publish directory:** `.` or `sri-vijaya-nursing-home` (root folder).

### B. Traditional Apache or Nginx Web Host (cPanel / Hostinger / GoDaddy)
1. Compress all files inside `sri-vijaya-nursing-home` into a `.zip` archive.
2. Upload and extract into the `public_html/` folder on your web host.
3. Ensure `.htaccess` (Apache) or `nginx.conf` is configured to serve `404.html` on missing pages:
   ```apache
   # Apache .htaccess snippet
   ErrorDocument 404 /404.html
   ```

---

## 4. Custom Domain & HTTPS Setup

1. In your domain registrar (e.g. GoDaddy, Namecheap, Cloudflare Registrar), point your DNS records:
   - For Netlify / Vercel / Cloudflare Pages: Add `CNAME` pointing to the designated host URL.
   - For traditional hosting: Point an `A` record to your server's public IP address.
2. Ensure an **SSL / TLS certificate** (such as Let's Encrypt) is activated so the site runs securely via `https://`.
3. In `index.html`, `about.html`, `services.html`, `doctors.html`, `contact.html`, `branches/*.html`, `robots.txt`, and `sitemap.xml`, replace all placeholder URLs (`https://www.example.com`) with the actual live domain (e.g., `https://www.srivijayanursinghome.com`).

---

## 5. Contact Form Configuration

The enquiry form on `contact.html` is currently built with client-side validation and displays a transparent disclosure that a backend handler must be connected before form messages reach hospital reception.

To make the form submit real patient messages:
1. **Option 1: Formspree (No Code)**
   - Sign up at [formspree.io](https://formspree.io).
   - Create a new form and copy the endpoint URL (e.g. `https://formspree.io/f/xyzabcde`).
   - In `contact.html`, set `<form action="https://formspree.io/f/xyzabcde" method="POST">`.
2. **Option 2: Netlify Forms**
   - Add the attribute `data-netlify="true"` and `name="contact"` to `<form>`.
   - Submissions will appear in your Netlify dashboard automatically.
3. **Option 3: WhatsApp Direct Integration**
   - A button linking to `https://wa.me/919063276907?text=Hello%20Sri%20Vijaya%20Nursing%20Home` can be enabled to allow direct mobile messaging for patients.

---

## 6. Local SEO & Search Console Setup Guide

To ensure high visibility when patients search for *"Gynaecologist in Kothagudem"*, *"Nursing Home Palvancha"*, or *"Maternity Hospital Bhadradri Kothagudem"*:

1. **Verify Google Search Console:**
   - Add property at [search.google.com/search-console](https://search.google.com/search-console).
   - Verify ownership via DNS TXT record or HTML meta tag.
   - Submit the sitemap URL: `https://yourdomain.com/sitemap.xml`.
2. **Claim Google Business Profiles (GBP):**
   - Create two distinct Google Business Profiles:
     - Profile 1: **Sri Vijaya Nursing Home – Kothagudem**
     - Profile 2: **Sri Vijaya Nursing Home – Palvancha**
   - Ensure the primary category is set to **"Nursing Home"** or **"Hospital"** or **"Gynecologist"**.
   - Set the website link for Profile 1 to `https://yourdomain.com/branches/kothagudem.html`.
   - Set the website link for Profile 2 to `https://yourdomain.com/branches/palvancha.html`.
   - Verify phone number `90632 76907` for Palvancha.
3. **NAP Consistency (Name, Address, Phone):**
   - Ensure the hospital name, physical address, and telephone number match exactly across the website, Google Business Profile, Justdial, Practo, and local directory citations.

---

## 7. Checklist of Hospital Information Requiring Confirmation

Before official public launch, please confirm the following details with Sri Vijaya Nursing Home management:

- [ ] **Exact Address – Kothagudem:** Street name, building number, road, and nearby landmark for the main branch.
- [ ] **Exact Address – Palvancha:** Street name, door number, and landmark for the Palvancha clinic.
- [ ] **Telephone Line – Kothagudem:** Official landline / mobile contact number for the Kothagudem facility.
- [ ] **Doctor Credentials & Registration:** Medical council registration numbers (e.g., TSMC/MCI), degrees (MBBS, DGO, MS/MD, FMAS), and titles for Dr. Vijaya Lakshmi and any visiting surgeons/specialists.
- [ ] **Consultation & OPD Timings:** Specific morning and evening OPD hours for both branches, including Sunday / holiday schedules.
- [ ] **Emergency & Maternity Admission Policy:** Confirmation whether 24/7 labor/delivery admissions are supported at the Kothagudem branch.
- [ ] **Diagnostic Facilities:** Clarify whether ultrasound scan, lab diagnostics, and pharmacy facilities are on-site or affiliated with partner centers.
- [ ] **Health Schemes / Insurance:** Clarification of Aarogyasri, EHS, or private health insurance TPA empannelment status.
