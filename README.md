# DataFlow — AI-Driven Document-to-Video SaaS Platform

A premium, high-converting, fully responsive landing page for **DataFlow**, an advanced AI-driven document-to-video automation engine. Built using vanilla web technologies, the page features smooth micro-interactions, realistic gained-height physics shadows, hardware-accelerated animations, and robust SEO hygiene.

---

## 🚀 Key Features

* **Interactive Studio Simulator**: A simulated document-to-video studio where users can select document files (`.docx`, `.xlsx`, `.pdf`), choose AI narrator voices, and trigger real-time simulated script rendering and voiceover playbacks.
* **Bento Grid Showcase**: A premium grid layout highlighting core product features (Automated Layouts, GPU Clustering, interactive 3D charts, and connectors) that responsively collapses into a touch-friendly interactive Accordion layout on mobile.
* **Pricing Matrix with Currency Converter**: A solid-black interactive pricing tier selector featuring a dynamic Billing Cycle Toggle (Monthly vs. Annual) and a real-time Currency Dropdown Selector (USD, EUR, GBP, JPY).
* **Testimonials & Carousel Slider**: A touch-swipeable review slider with custom navigation nodes showcasing client feedback and partner trust logos.
* **Hardware-Accelerated Backgrounds**: Fluid float-animated SVG cube particles, glowing background orbs, and a high-definition looping background video canvas.

---

## 🛠️ Tech Stack & Rules

* **Core**: Semantic HTML5 & Modern Vanilla JavaScript (ES6+).
* **Styling**: Vanilla CSS3 utilizing CSS custom properties for styling tokens and system constants.
* **Animations**: Native CSS transitions, `@keyframes` transforms, and the Web Animations API (WAAPI).
* **Typography**: Google Fonts — `JetBrains Mono` (headers, code panels, variables) + `Inter` (body, controls).
* **Icons**: Optimized, inlined inline SVGs to achieve zero network icon requests.
* **Zero Dependencies**: 100% free of heavy libraries such as Framer Motion, Radix, Tailwind CSS, or pre-built animation engines.

---

## ⚡ Performance Optimizations

1. **Scroll-Adaptive Compositing**: To eliminate scroll and rendering lag, `backdrop-filter: blur(16px)` on the sticky header is disabled at `scrollY <= 20`. A scroll listener toggles the blur filter only as the user scrolls away from the playing video.
2. **IntersectionObserver Rendering Control**: Built observers that monitor the `#hero-canvas` and background video. They dynamically pause canvas frames and video playback when they scroll out of view, offloading GPU/CPU cycles.
3. **GPU-Decoded Background Video**: Utilizes the original video asset `hero.mp4` set to hardware acceleration layers (`transform: translate3d(0,0,0)` and `will-change: transform`) and optimized with viewport-scroll observers.
4. **Gained-Height Physics Shadows**: Hover cards utilize physical elevation offsets (`translateY(-6px)`) coupled with diffused, spread-out shadow vectors to mimic light dispersion.

---

## 🔍 SEO & Accessibility Hygiene

* **Single `<h1>` Tag**: Strict outline architecture with exactly one primary `<h1>` tag containing keyword-rich taglines.
* **JSON-LD Schema Markup**: Integrated structured metadata inside the `<head>` to define `SoftwareApplication` ratings, offerings, and search properties.
* **Descriptive Testing IDs**: All navigation, drawer, and interactive buttons contain unique `id` selectors (`#logo-link`, `#nav-link-simulator`, etc.) to facilitate automated browser testing (Cypress, Selenium).
* **Aria Accessibility Attributes**: Nav elements, buttons, and drawers use appropriate `aria-label`, `aria-hidden`, `aria-expanded`, and `role` descriptors.

---

## 🎨 Approved Color Palette

| Color | Hex Code | Utility |
| :--- | :--- | :--- |
| **Forsythia** | `#FFC801` | Primary Accent, CTAs, Highlights |
| **Deep Saffron** | `#FF9932` | Secondary Accent, Hover states, Gradients |
| **Nocturnal Expedition** | `#114C5A` | Dark Teal, Nav elements, Dark sections |
| **Oceanic Noir** | `#172B36` | Deep Dark Blue, Main Background |
| **Mystic Mint** | `#D9E8E2` | Soft Mint, Accents, Muted Text |
| **Arctic Powder** | `#F1F6F4` | Light Gray, Clean light blocks |
| **White** | `#FFFFFF` | Core text, titles |
| **Black** | `#000000` | Pricing section background |

---

## 💻 Local Preview & Development

You can open the page directly from the filesystem or host it locally.

### Direct Opening
Open the landing page directly by double-clicking:
`index.html`

### Hosting via Python
Start a lightweight local server to preview responsively on your phone or local network:
```bash
# Start python HTTP server on port 8080 binding to all interfaces
python -m http.server 8080 --bind 0.0.0.0
```
Open your browser and navigate to:
`http://localhost:8080/index.html`
