# MyHealth: Design notes for Section 10 (Style, Colour, Animation, Fonts, Logo)

Use this when writing up **Section 10: Choice of style, colour, animation, fonts** in your report and on your Wix site.

**Prototype alignment with high-fidelity wireframes:** The clickable prototype mirrors the high-fi dashboard: "Today" + date header, Important reminders first, Next Medication Reminder card with **Taken** button, Upcoming Appointment with chevron, Medication today (adherence ring), and a 5-item bottom nav (Home, Meds, Appts, Chat, Settings). Grayscale accents (dark grey nav bar, grey reminder card, Taken button style) match the wireframe aesthetic. Separate **Login** and **Create account** pages are included; **Add appointment** has its own form (Doctor/Clinic, Date, Time, Location, Notes); medication list rows have a **Mark taken** / **Taken** toggle button.

---

## Logo

- **Wordmark:** “MyHealth” in bold, primary blue.
- **Icon:** Heart outline (simple line icon, no fill). Represents care and health; friendly and recognizable.
- **Placement:** Logo + icon appear in the header on every screen and on the welcome screen (larger).
- **File:** The prototype uses an inline SVG heart. For a final logo you can export as SVG/PNG and replace.

---

## Colour

| Role        | Hex       | Use |
|------------|-----------|-----|
| **Primary** | `#2563eb` | Buttons, links, logo, active nav, focus rings. Trust and clarity. |
| **Primary hover** | `#1d4ed8` | Button hover state. |
| **Primary light** | `#dbeafe` | Active nav background, focus glow. |
| **Success** | `#059669` | “Taken” badges, confirmations, success states. |
| **Success light** | `#d1fae5` | Success badge background. |
| **Background** | `#f8fafc` | Page background (light grey). |
| **Surface** | `#ffffff` | Cards, inputs, phone frame. |
| **Border** | `#e2e8f0` | Card and input borders, dividers. |
| **Text** | `#1e293b` | Primary body and headings. |
| **Text muted** | `#64748b` | Secondary text, captions, back links. |

**Rationale:** Blue for trust and clarity; green for success/confirmation only. Neutrals for readability. No harsh red except for critical alerts (e.g. missed dose) if you add them later.

---

## Typography (fonts)

- **Font stack:** `'Segoe UI', system-ui, -apple-system, sans-serif`
- **Sizes:**  
  - Large (section titles): `1.125rem`  
  - Base (body, buttons): `1rem`  
  - Small (captions, nav, secondary): `0.875rem`
- **Weights:** Regular (400), medium (500), semibold (600), bold (700).
- **Rationale:** Sans-serif for readability; system fonts load fast and are accessible. For Wix you can switch to Inter or another clean sans and keep the same sizes.

---

## Style (overall)

- **UI style:** Clean, minimal, clear hierarchy.
- **Shapes:** Rounded corners (12px cards/buttons, 8px small elements).
- **Spacing:** Ample padding; tap targets at least 44–48px high.
- **Iconography:** Simple line icons (heart for logo; you can add pill, calendar, reminder icons consistently later).

---

## Animation

- **Transitions:** `0.2s ease` on buttons, links, cards (background, border, color).
- **Button press:** Slight scale on active (`transform: scale(0.98)`) for tap feedback.
- **Hover:** Colour and background changes only; no heavy motion.
- **Future:** You can add a short transition when “logging” a medication (e.g. checkmark appear) or between screens if you move to a single-page app.

---

## How to add the prototype to Wix

1. **Host the prototype**  
   Upload the `prototype` folder (all HTML + `styles.css`) to:
   - **Wix:** Create a new page, add an “Embed” element, and paste the URL of your hosted prototype (e.g. from Wix’s own hosting or a subdomain), **or**
   - **External host:** e.g. GitHub Pages, Netlify, or your school’s web space. Upload the folder so `index.html` is the entry point.

2. **Link from Wix**  
   - Add a button or text link (e.g. “Try the prototype” or “Clickable prototype”) that opens the prototype URL in a new tab (`target="_blank"`).  
   - If your host supports iframes and allows embedding, you can use Wix’s “Embed” / iframe and paste the prototype URL so it appears inside the page.

3. **Entry URL**  
   The link you share should be the URL of `index.html` (e.g. `https://yoursite.com/prototype/` or `https://yoursite.com/prototype/index.html`). Users land on Welcome → Log in → Home, then can tap through Meds, Add medication, Appointments, and Appointment details.
