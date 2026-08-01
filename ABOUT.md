# About SafariMaster Landing Page

Welcome to **SafariMaster** — the premier tour operations SaaS platform custom-engineered for safari operators, Destination Management Companies (DMCs), and travel agencies across East Africa and global luxury wildlife markets.

This document provides a complete overview of the SafariMaster landing page architecture, design system, core capabilities, and frontend engineering specifications.

---

## 1. Core Purpose & Value Proposition

SafariMaster bridges the gap between client experience and back-office financial rigor. Traditional tour operators often rely on fragmented spreadsheets, disconnected PDF quotes, and manual bank reconciliations. SafariMaster unifies the entire safari lifecycle into one real-time workspace.

### Primary Operational Pillars
* **Quote-to-Invoice Speed**: Turn itinerary inquiries into client-ready branded quotes and tax invoices in under 2 minutes.
* **Supplier & Reservation Management**: Generate instant lodge, park fee, flight, and transfer vouchers with live barcode verification.
* **Financial Reconciliation Confidence**: Link every deposit wire, MPESA payment, lodge receipt, and supplier payout back to its parent trip file.
* **Multi-Tenant Governance**: Empower multi-brand DMCs to manage separate tenant accounts with independent document numbering, logos, and audit trails.

---

## 2. Landing Page Structural Blueprint

The SafariMaster landing page is designed as an interactive, single-page application experience with smooth navigation and real-time visual feedback:

### Section Breakdown
1. **Header & Navigation**
   * Brand identity with luxury safari iconography
   * Smooth-scrolling section links (`Product`, `Pipeline`, `Modules`, `Finance`, `Governance`)
   * Theme switcher (Dark / Light mode) with system preference detection
   * Mobile-responsive slide-out drawer with 44px+ touch targets and full keyboard trapping
2. **Hero Section**
   * Confidence-driven headline using fluid clamp typography (`.h1-display`)
   * Interactive 5-tile floating glassmorphic workspace cluster representing Quotes, Invoices, Mara Bookings, Lodge Vouchers, and Net Margin
   * Live workspace sync indicator badge with subtle pulsing animation
3. **Operations Pipeline (Interactive Vertical Timeline)**
   * 6-step lifecycle tracker: **Inquiry & Itinerary**, **Instant Quote**, **Tax Invoice**, **Lodge Vouchers**, **Supplier Payouts**, and **Reconciliation**
   * Real-time active step highlights and detail panels
4. **Core Capabilities Bento Grid**
   * 6 modular cards highlighting Quotation Engine, Reservation Vouchers, Bank & MPESA Match, Custom Branding, Profitability Analytics, and DMC Governance
5. **Finance & Reconciliation Deep Dive**
   * Real-time payment matching simulator with interactive progress indicator and live score calculation
6. **Multi-Tenant Governance Section**
   * Visual representation of tenant isolation, audit trails, and workspace switching
7. **Branded Documents Suite Showcase**
   * Live preview cards of branded Quotations, Tax Invoices, Official Receipts, and Reservation Vouchers
8. **Call-to-Action (CTA) Banner & Demo Modal**
   * High-contrast booking prompt launching a responsive modal form with live submission handling
9. **Footer**
   * Comprehensive link groups (Product, Company, Legal, Security) and social handles

---

## 3. Design System & Typographic Standards

The landing page follows strict mathematical design principles to convey luxury, trust, and enterprise capability without visual noise.

### Color Palette Tokens
| Token Name | Hex / Class | Primary Use Case |
| :--- | :--- | :--- |
| **Terracotta Accent** | `#C85A32` (`.text-terracotta`, `.bg-terracotta`) | Brand highlights, active states, call-to-action buttons |
| **Ochre Highlight** | `#D97706` (`.text-amber-500`) | Secondary badges, warning states |
| **Emerald Growth** | `#10B981` (`.text-emerald-500`) | Profit margins, matched payments, confirmed statuses |
| **Charcoal Surface** | `--sm-surface` | Clean, high-contrast dark/light container surfaces |
| **Border Soft** | `--sm-border` | Precise 1px hairline borders |

### Typographic Hierarchy
* **`.h1-display`**: Fluid clamp headline scale (`clamp(2.25rem, 5vw, 3.75rem)`) for bold hero authority.
* **`.h2-display`**: Section headings (`clamp(1.75rem, 3.5vw, 2.5rem)`) with tight tracking (`-0.025em`).
* **`.h3-heading`**: Card and module title font styling.
* **`.eyebrow`**: Uppercase tracking badge styling (`0.05em` letter spacing) for category tags.
* **`.stat-number`**: Tabular numeral font feature settings (`tnum`, `zero`) ensuring perfect numerical alignment in monetary tables.

---

## 4. Mobile Responsiveness & Technical Specifications

* **Viewport Compliance**: Tested and optimized for 390px mobile viewports without any horizontal scroll or clipping.
* **Bento Grid Collapse**: Responsive single-column vertical stack with logical reading order on small displays.
* **Tap Target Minimums**: Every button, link, and toggle maintains a minimum hit area of `44px x 44px`.
* **Motion & Performance**:
  * `prefers-reduced-motion` CSS rules pause all idle float and pulse animations for users with motion sensitivity.
  * Lazy loading attributes (`loading="lazy"`) and explicit width/height dimensions on images prevent Layout Shift (CLS).

---

## 5. Metadata & Accessibility Standards

* **Semantic Landmarks**: Includes `<header>`, `<main id="main-content">`, `<nav>`, `<section>`, and `<footer>` tags.
* **Keyboard Accessibility**:
  * Screen-reader Skip Link (`#main-content`)
  * Distinct outline focus rings (`outline: 2px solid var(--sm-terracotta)`)
  * Full `aria-label`, `aria-expanded`, and `aria-controls` bindings on mobile drawers and modal triggers.
* **Structured Data**:
  * Full Schema.org `SoftwareApplication` JSON-LD payload.
  * Open Graph and Twitter Card tags for social media link previews.

---

*SafariMaster — Engineering precision for modern safari operators.*
