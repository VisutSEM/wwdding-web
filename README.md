# Sakkada & Sovannary | Khmer Wedding Web-App 💍✨

A responsive, database-free, client-side Khmer Wedding Web Application crafted with traditional royal aesthetics, bilingual support (Khmer & English), live wedding countdown, Bakong KHQR digital envelope gift center, zero-dependency ambient Web Audio synthesizer, pre-wedding photo gallery with lightbox, guestbook with LocalStorage, and interactive QR code generator for print and social sharing.

---

## 🌸 Features

1. **Royal Khmer Aesthetics & Design System**
   - Palette: Royal Wine (`#6D071A`, `#4A0410`), Traditional Gold (`#D4AF37`, `#E6CA65`), Lotus & Cream (`#FAF6F0`, `#FFFBF5`).
   - Typography: `Kantumruy Pro` (Khmer), `Playfair Display` (Classic Serif), `Great Vibes` (Romantic Script).
   - Canvas animation: floating lotus petals and golden sparkling stars.

2. **Hero & Ceremony Showcase**
   - Circular portraits of bride and groom with metallic gold ring borders.
   - Traditional floral / kbach ornamental header.
   - Live countdown timer targeting the wedding date (Sunday, November 29, 2026).

3. **Parents' Honor & Traditional Khmer Wedding Timeline**
   - Formal invitation text honoring both families.
   - 5-step traditional timeline (Fruit Procession, Betel Nut Ceremony, Hair Cutting, Candle Passing & Wrist-Tying, Evening Banquet).

4. **Pre-Wedding Photo Gallery & Lightbox**
   - Responsive photo grid with hover zoom & overlays.
   - Fullscreen zero-dependency lightbox modal with keyboard navigation (`ESC`, `←`, `→`).

5. **Venue & Transportation Guide**
   - Embedded Google Map for The Premier Centre Sen Sok (Phnom Penh).
   - Fast booking shortcuts for PassApp and Grab.

6. **Digital Envelope / KHQR Gift Center**
   - High-fidelity Bakong standard KHQR cards for ABA Bank (USD) & ACLEDA Bank (KHR).
   - One-click "Copy Account Number" with instant toast feedback.
   - Fast-access digital envelope modal from top navigation.

7. **Romantic Ambient Web Audio Synthesizer**
   - Zero-asset Cambodian pentatonic harp synthesizer powered by the native Web Audio API.
   - Synchronized spinning vinyl record and animated equalizer bars.

8. **Wishes Wall / Guestbook**
   - Client-side guestbook with emoji quick inserters and floating heart keyframe animations.
   - Persisted locally with `localStorage`.

9. **QR Code Generator & Social Sharing**
   - Generates live QR code linking directly to the web app.
   - One-click "Download QR Code" for printing on physical paper cards.
   - Instant Telegram sharing.

---

## 🚀 Free Deployment Guide

### Option A: GitHub Pages
1. Initialize a git repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of Khmer Wedding Web-App"
   ```
2. Create a repository on GitHub (e.g., `wedding-invitation`).
3. Push to GitHub:
   ```bash
   git remote add origin https://github.com/<your-username>/wedding-invitation.git
   git branch -M main
   git push -u origin main
   ```
4. On GitHub, go to **Settings > Pages > Branch: main > Save**.
5. Your wedding invitation will be live at:
   `https://<your-username>.github.io/wedding-invitation/`

### Option B: Vercel or Cloudflare Pages
1. Log in to [Vercel](https://vercel.com) or [Cloudflare Pages](https://pages.cloudflare.com).
2. Drag and drop this folder or connect your GitHub repository.
3. Deploy instantly with zero configuration!
4. (Optional) Connect your custom wedding domain (e.g. `sakkada-sovannary-wedding.com`).

---

## 🎨 Asset Structure
```text
wedding-app/
├── index.html
├── README.md
├── task/
│   └── task.md
└── assets/
    ├── og-banner.jpg
    ├── music/
    └── images/
        ├── groom.jpg
        ├── bride.jpg
        ├── aba-khqr.png
        ├── acleda-khqr.png
        └── prewedding/
            ├── photo-1.jpg
            ├── photo-2.jpg
            ├── photo-3.jpg
            └── photo-4.jpg
```
