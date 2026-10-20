# Khmer Wedding Web-App Implementation Plan (No-Database Architecture)

A detailed, step-by-step checklist to build, customize, test, and deploy a responsive, database-free Khmer Wedding web application with traditional aesthetics, bilingual support, KHQR digital envelope, and interactive animations.

---

## Phase 1: Asset Preparation & Project Scaffolding

- [x] **1.1. Create Repository & File Structure**
  - [x] Initialize project directory (`khmer-wedding-app/` / root workspace).
  - [x] Create core files and folders:
    ```text
    khmer-wedding-app/
    ├── index.html
    ├── assets/
    │   ├── images/
    │   │   ├── groom.jpg
    │   │   ├── bride.jpg
    │   │   ├── prewedding/
    │   │   │   ├── photo-1.jpg
    │   │   │   ├── photo-2.jpg
    │   │   │   ├── photo-3.jpg
    │   │   │   └── photo-4.jpg
    │   │   ├── aba-khqr.png
    │   │   └── acleda-khqr.png
    │   ├── music/ (optional MP3 if replacing synthesizer)
    │   └── og-banner.jpg (1200x630 social share preview)
    └── README.md
    ```

- [x] **1.2. Design System & Typography Setup**
  - [x] Import Google Fonts:
    - `Kantumruy Pro` (Primary Khmer font for crisp, modern readability).
    - `Playfair Display` (Classic serif for names and dates).
    - `Great Vibes` (Romantic calligraphy for couple headers).
  - [x] Configure Tailwind CSS color tokens:
    - Royal Wine: `#6D071A` & `#4A0410`
    - Traditional Gold: `#D4AF37`, `#E6CA65`, `#A47E2F`
    - Lotus / Cream Surface: `#FAF6F0`, `#FFFBF5`
  - [x] Include Lucide Icons CDN script (`lucide.createIcons()`).

---

## Phase 2: Core Layout & Hero Section

- [x] **2.1. Floating Controls Header**
  - [x] Build fixed top-right pill bar with backdrop blur (`backdrop-blur-md`).
  - [x] Implement language switcher button (`KM` ⇄ `EN`).
  - [x] Implement audio player button with spinning vinyl disk animation and equalizer bars.

- [x] **2.2. Hero & Couple Presentation**
  - [x] Insert traditional floral/kbach SVG ornament header.
  - [x] Add couple names with golden gradient styling.
  - [x] Build circular portrait frames with gold metallic ring borders.
  - [x] Add bride & groom bilingual labels (កូនកំលោះ / The Groom & កូនក្រមុំ / The Bride).
  - [x] Include event date and venue subtitle.

- [x] **2.3. Live Countdown Timer**
  - [x] Set target wedding timestamp in JavaScript (`new Date('YYYY-MM-DDTHH:MM:SS+07:00')`).
  - [x] Calculate Days, Hours, Minutes, and Seconds.
  - [x] Implement 1-second interval loop with auto-zero fallback on event arrival.
  - [x] Style countdown digits into four cream-colored frosted cards.

- [x] **2.4. Quick Anchor Action Bar**
  - [x] Add fast-scroll pill buttons: _Ceremony Schedule_, _Venue & Map_, _Digital Envelope (KHQR)_.

---

## Phase 3: Content Sections & Cultural Components

- [x] **3.1. Parents' Blessing & Honor Section**
  - [x] Add traditional formal Khmer invitation wording.
  - [x] Display groom's parents (មាតាបិតាខាងកូនកំលោះ) and bride's parents (មាតាបិតាខាងកូនក្រមុំ) in side-by-side cards.

- [x] **3.2. Traditional Khmer Wedding Timeline (កាលវិភាគពិធីបុណ្យ)**
  - [x] Build vertical timeline layout with gold connector lines and marker dots.
  - [x] Step 1 (07:00 AM): ពិធីហែជំនូន & កាត់ផ្លែឈើ (Fruit & Gift Procession).
  - [x] Step 2 (08:30 AM): ពិធីពិសាស្លា & សំពះផ្ទឹម (Betel Nut Ceremony & Union).
  - [x] Step 3 (10:00 AM): ពិធីកាត់សក់បង្កក់សិរី (Hair Cutting Cleansing Ritual).
  - [x] Step 4 (11:30 AM): ពិធីបង្វិលពពិល & ចងដៃ (Candle Passing & Red String Wrist-Tying).
  - [x] Step 5 (05:00 PM): ពិធីជប់លៀងពិសាភោជនាហារ (Evening Reception & Banquet).

- [x] **3.3. Pre-Wedding Photo Gallery & Lightbox**
  - [x] Build responsive photo grid (2 columns mobile, 3 columns desktop).
  - [x] Add hover zoom and overlay icon effects.
  - [x] Implement zero-dependency JavaScript Lightbox:
    - Click image to open full-screen modal with dark blurred backdrop.
    - Click `ESC`, backdrop, or `✕` icon to close.

- [x] **3.4. Location, Maps & Transportation Guide**
  - [x] Embed Google Maps iframe for venue (e.g., The Premier Centre Sen Sok, Phnom Penh).
  - [x] Add direct "Open in Google Maps" external link button.
  - [x] Add PassApp / Grab ride-hailing booking shortcut link.

---

## Phase 4: Interactive Client-Side Features (No Database)

- [x] **4.1. Digital Envelope / KHQR Gift Center**
  - [x] Build high-fidelity KHQR card matching Bakong standards:
    - Red KHQR header banner.
    - ABA Mobile account holder name and account number.
    - ACLEDA Bank account details.
  - [x] Implement one-click "Copy Account Number" button using `navigator.clipboard.writeText()` with temporary "Copied! ✓" toast animation.
  - [x] Add dedicated pop-up modal version for instant access from navigation.

- [x] **4.2. Romantic Ambient Audio Player (Zero Asset Web Audio Synth)**
  - [x] Implement audio toggle using native Web Audio API (triangle wave oscillator).
  - [x] Play a soft Cambodian pentatonic harp sequence without requiring external MP3 bandwidth or licensing issues.
  - [x] Synchronize vinyl disc rotation and sound bar animations with play/pause state.

- [x] **4.3. Client-Side Guestbook / Wishes Wall**
  - [x] Build form with Name, Relationship selector, and Blessing message textarea.
  - [x] Add one-click emoji blessing inserters (💐, 💍, ❤️, 🥂, 🙏).
  - [x] Write `handleSendWish()` function to sanitize inputs (`escapeHtml`) and prepend new wish cards dynamically to the DOM.
  - [x] Add floating heart CSS keyframe animation upon submission.

- [x] **4.4. Canvas Lotus Petals & Gold Sparkles Animation**
  - [x] Add full-screen HTML5 `<canvas id="petals-canvas">` with `pointer-events: none`.
  - [x] Create `Petal` particle class with natural drifting trajectory, rotation, and gentle sway.
  - [x] Render 20–25 lightweight petals in gold and soft lotus-pink hues with `requestAnimationFrame`.

---

## Phase 5: Bilingual Support & Responsive Tuning

- [x] **5.1. Bilingual Dictionary Hookup**
  - [x] Tag all translatable DOM elements with `data-km="..."` and `data-en="..."`.
  - [x] Implement `toggleLanguage()` to cycle through text content smoothly without page reload.
  - [x] Verify Khmer fonts display proper line-height without clipping subscripts (ជើងអក្សរ).

- [x] **5.2. Mobile Responsiveness & Performance Audit**
  - [x] Test layout on mobile viewports (iPhone SE, iPhone 14/15 Pro, Samsung Galaxy).
  - [x] Ensure tap targets (buttons, links, QR cards) are at least 44x44px.
  - [x] Verify horizontal scrolling is completely eliminated on small viewports (`overflow-x: hidden`).
  - [x] Compress all pre-wedding images (convert to `.webp` or optimize JPGs under 200KB each).

---

## Phase 6: Social Meta Tags & Free Deployment

- [x] **6.1. OpenGraph & Social Sharing Meta Tags**
  - [x] Add essential `<head>` tags for Telegram, WhatsApp, and Facebook Messenger preview:
    ```html
    <meta
      property="og:title"
      content="មង្គលការ | Dara & Sothea Wedding Invitation"
    />
    <meta
      property="og:description"
      content="សូមគោរពអញ្ជើញចូលរួមពិធីមង្គលការរបស់យើងខ្ញុំ នៅថ្ងៃអាទិត្យ ទី២៩ ខែវិច្ឆិកា ឆ្នាំ២០២៦"
    />
    <meta
      property="og:image"
      content="https://your-domain.com/assets/og-banner.jpg"
    />
    <meta property="og:type" content="website" />
    ```

- [x] **6.2. Free Deployment Options**
  - [x] **Option A (GitHub Pages):**
    - [x] Create GitHub repository `wedding-invitation`.
    - [x] Push `index.html` and `assets/`.
    - [x] Go to **Settings > Pages > Branch: main > Save**.
    - [x] Access live URL at `https://<username>.github.io/wedding-invitation/`.
  - [x] **Option B (Vercel / Cloudflare Pages):**
    - [x] Drag and drop folder into Vercel / Cloudflare Pages dashboard.
    - [x] Connect custom wedding domain (e.g., `dara-sothea-wedding.com`).

- [x] **6.3. QR Code Generation for Physical Cards**
  - [x] Generate print-ready QR code linking to the live web app URL.
  - [x] Print QR code on physical paper invitations for guests to scan and view details.
