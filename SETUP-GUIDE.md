# Nibblix India Website — Setup Guide

## 📧 EmailJS Setup (5 minutes, one-time)

The contact form sends emails directly to abhishek.keskar977@gmail.com using EmailJS.

### Step 1: Create EmailJS Account
1. Go to **https://www.emailjs.com** → Click **Sign Up** (it's free)
2. Sign up with any email

### Step 2: Get your Public Key
1. Go to **Account** (top menu)
2. Copy your **Public Key** (looks like: `user_aBcDeFgHiJkLmN`)
3. Open `index.html` → Find this line:
   ```
   emailjs.init('YOUR_PUBLIC_KEY');
   ```
4. Replace `YOUR_PUBLIC_KEY` with your actual key

### Step 3: Add Gmail Service
1. Go to **Email Services** → Click **Add New Service**
2. Choose **Gmail**
3. Connect **abhishek.keskar977@gmail.com**
4. Click **Create Service**
5. Copy the **Service ID** (looks like: `service_abc123`)
6. In `index.html`, replace `YOUR_SERVICE_ID` with this ID

### Step 4: Create Email Template
1. Go to **Email Templates** → Click **Create New Template**
2. Set the template like this:
   - **Subject:** `New Website Inquiry from {{from_name}}`
   - **Body:**
     ```
     You received a new inquiry from NibblixIndia.com:

     Name: {{from_name}}
     Company: {{company}}
     Email: {{reply_to}}
     Phone: {{phone}}

     Message:
     {{message}}
     ```
   - **To Email:** `abhishek.keskar977@gmail.com`
3. Click **Save**
4. Copy the **Template ID** (looks like: `template_xyz789`)
5. In `index.html`, replace `YOUR_TEMPLATE_ID` with this ID

### Done! Test it by submitting the form on your website.

---

## 🔗 Social Media Links

In `index.html`, search for `href="#"` and replace with actual URLs:
- Instagram: Replace `href="#"` next to `title="Instagram"` with your Instagram URL
- LinkedIn: Replace `href="#"` next to `title="LinkedIn"` with your LinkedIn URL

There are 4 places total (2 in nav, 2 in footer).

---

## 🚀 Deploy on GitHub Pages (free hosting)

### Step 1: Create GitHub Repository
1. Go to **github.com** → Sign in → Click **New Repository**
2. Name it: `nibblixindia`
3. Make it **Public**
4. Click **Create repository**

### Step 2: Upload Files
1. Click **"uploading an existing file"**
2. Drag ALL files and folders from this unzipped package into the upload area:
   - `index.html`
   - `images/` folder (with team/ and branches/ inside)
   - `docs/` folder (with all PDFs)
   - `SETUP-GUIDE.md` (optional)
3. Click **Commit changes**

### Step 3: Enable GitHub Pages
1. Go to **Settings** → **Pages** (left sidebar)
2. Source: **Deploy from a branch**
3. Branch: **main** → folder: **/ (root)**
4. Click **Save**
5. Wait 1-2 minutes → your site is live at:
   `https://YOUR-USERNAME.github.io/nibblixindia`

### Step 4: Connect NibblixIndia.com Domain (optional)
1. In GitHub Pages settings, under **Custom domain**, enter: `NibblixIndia.com`
2. Go to your domain registrar (GoDaddy, Namecheap, etc.)
3. Add these DNS records:
   - Type: **A** → Value: `185.199.108.153`
   - Type: **A** → Value: `185.199.109.153`
   - Type: **A** → Value: `185.199.110.153`
   - Type: **A** → Value: `185.199.111.153`
   - Type: **CNAME** → Name: `www` → Value: `YOUR-USERNAME.github.io`
4. Wait 24-48 hours for DNS to propagate
5. Back in GitHub Pages, check **Enforce HTTPS**

---

## 📁 File Structure

```
nibblixindia/
├── index.html                          ← Main website
├── SETUP-GUIDE.md                      ← This file
├── images/
│   ├── team/
│   │   ├── abhishek-keskar.jpeg
│   │   ├── mayawati-chakre.jpeg
│   │   ├── sakshi-shinde.jpeg
│   │   ├── vighnesh-divekar.jpeg
│   │   ├── vaishnavi-surushe.jpeg
│   │   └── punam-dakore.jpeg
│   ├── branches/
│   │   ├── bigshort-counter.jpeg
│   │   ├── amul-counter.jpeg
│   │   ├── infosys-counter.jpeg
│   │   └── mercedes-counter.jpeg
│   └── logos/                          ← Add brand logos here
└── docs/
    ├── certificate-of-incorporation.pdf
    ├── gst-certificate.pdf
    ├── fssai-food-license.pdf
    ├── pan-card.pdf
    ├── udyam-registration.pdf
    ├── provident-fund.pdf
    ├── esic-registration.pdf
    ├── tan-certificate.pdf
    └── din-approval.pdf
```

---

© 2026 Nibblix India Pvt Ltd | Built with care
