# REPZ — Landing Page Redesign Specification
**Version:** 2.0
**Date:** Março 2026
**Objective:** Increase free-account signups (create account → test product)
**Primary CTA:** Criar conta grátis (Free up to 4 students, no credit card)

---
---

# DELIVERABLE 1: INFORMATION ARCHITECTURE

## Section Map (scroll order)

| # | Section | Purpose | Key Message | Primary CTA |
|---|---------|---------|-------------|-------------|
| 1 | **Header + Sticky Nav** | Navigation + persistent conversion point | Brand presence + always-visible signup path | `Criar conta grátis` |
| 2 | **Hero** | First impression. Communicate value prop + eliminate risk | "Organize treinos, encante alunos, receba em dia. Grátis." | `Começar grátis agora` |
| 3 | **Proof Strip** | Instant credibility below the fold | Numbers or social proof statement | — |
| 4 | **Problem** | Create emotional identification with the pain | "Seu dia a dia não devia ser assim" | — |
| 5 | **Solution (3 Pillars)** | Show how Repz solves each pain point | Treinos + App do Aluno + Cobrança | `Criar conta grátis` |
| 6 | **How It Works** | Reduce friction by showing simplicity | 2-column step-by-step (Personal vs Aluno) | — |
| 7 | **First 30 Days** | Visualize fast time-to-value | Timeline from signup to full operation | — |
| 8 | **Testimonials** | Qualitative social proof | Real personal trainers recommending the platform | — |
| 9 | **Pricing** | Transparency + free plan as hero | Free highlighted, 2 paid tiers with "Pra quem é" | `Criar conta grátis` |
| 10 | **FAQ** | Break final signup objections | 6–8 answers to common hesitations | — |
| 11 | **Final CTA** | Last conversion opportunity | Risk-free recap + single CTA | `Criar minha conta grátis` |
| 12 | **Footer** | Legal, links, discreet roadmap | Navigation + trust + "Em breve" as roadmap block | — |

**Scroll depth strategy:**
Sections 1–3 convert impulsive visitors (above fold + first scroll).
Sections 4–7 convert analytical visitors (understand before acting).
Sections 8–10 convert skeptical visitors (need proof and transparency).
Section 11 catches anyone who scrolled the entire page without converting.

---
---

# DELIVERABLE 2: WIREFRAME BLUEPRINT

---

## Section 1: Header + Sticky Nav

```
┌─────────────────────────────────────────────────────────┐
│  [Logo: Repz]    Funcionalidades  Preços  FAQ   [CTA]   │
└─────────────────────────────────────────────────────────┘
```

**Layout:**
- Mobile: Logo left, hamburger right. CTA hidden in menu but appears as a sticky bottom bar on scroll.
- Desktop: Single row. Logo left. Nav links center. CTA button right.

**Components:**
- Logo (SVG, max-height 32px)
- 3 nav links (anchor scroll to Funcionalidades, Preços, FAQ)
- Primary CTA button: `Criar conta grátis`
- Desktop-only microcopy below CTA: "Sem cartão. Pronto em 2 min."

**Interaction notes:**
- Header becomes sticky after scrolling past the hero.
- On sticky state: background becomes solid white with subtle shadow (box-shadow: 0 1px 4px rgba(0,0,0,0.06)).
- Mobile: a fixed bottom bar with CTA appears after scrolling 300px. The bar includes the button + one-line microcopy.

**Content hierarchy:**
- Logo: brand weight only, no tagline
- Nav: body/small text, muted color
- CTA: primary button style, contrasting color

---

## Section 2: Hero

```
MOBILE (360px)                        DESKTOP (1280px+)
┌───────────────────────┐    ┌─────────────────────────────────────────┐
│     [Eyebrow pill]    │    │                                         │
│                       │    │  [Eyebrow pill]        ┌──────────────┐ │
│   H1 headline         │    │                        │              │ │
│   (2–3 lines)         │    │  H1 headline           │  Hero image  │ │
│                       │    │  (2 lines)             │  or app      │ │
│   Subhead paragraph   │    │                        │  mockup      │ │
│                       │    │  Subhead paragraph     │              │ │
│   ✅ Bullet 1         │    │                        │              │ │
│   ✅ Bullet 2         │    │  ✅ Bullet 1           └──────────────┘ │
│   ✅ Bullet 3         │    │  ✅ Bullet 2                            │
│                       │    │  ✅ Bullet 3                            │
│   [===== CTA =====]   │    │                                         │
│   Ver como funciona ↓ │    │  [===== CTA =====]  Ver como funciona ↓│
│                       │    │                                         │
│   microcopy line      │    │  microcopy line                         │
│                       │    │                                         │
│   ┌─────────────────┐ │    └─────────────────────────────────────────┘
│   │  Hero image /   │ │
│   │  app mockup     │ │
│   └─────────────────┘ │
└───────────────────────┘
```

**Layout:**
- Mobile: Single column, stacked. Text first, image below.
- Desktop: 2 columns (55% text left, 45% visual right).

**Components:**
- Eyebrow pill badge (small, colored background, uppercase or sentence case)
- H1 headline (2–3 lines max)
- Subhead (1 paragraph, max 2 sentences)
- 3 benefit bullets with checkmark icon
- Primary CTA button (full-width on mobile)
- Secondary CTA link (text link with arrow)
- Microcopy line (small, muted, below CTA)
- Hero visual: app mockup showing a workout screen, or lifestyle photo of trainer + phone

**Visual guidance:**
- Hero image should show the Repz app interface (workout screen on a phone) held by or near a personal trainer in a gym context. Avoid stock-photo feel. If using a real screenshot, overlay it on a device frame.
- Alternative: a clean 3D phone mockup showing the trainer dashboard on one side and the student app on the other.
- Background: subtle gradient or solid light color. No busy patterns.

**Content hierarchy:**
- Eyebrow: caption/overline size, accent color
- H1: largest text on the page (clamp between 32px mobile – 56px desktop)
- Subhead: body-large, muted color
- Bullets: body, icon + text, tighter line-height
- CTA: primary button, 48px+ height
- Microcopy: caption, lightest text weight

**Interaction notes:**
- Secondary CTA smooth-scrolls to "Como Funciona" section.
- On mobile, hero image lazy-loads below the fold to keep LCP fast.

---

## Section 3: Proof Strip

```
┌──────────────────────────────────────────────────────┐
│                                                      │
│   [XXX]+          [XXX]+          [XXX]+     4.8 ★   │
│   Personais       Treinos         Alunos     Nota    │
│   ativos          entregues       no app     no app  │
│                                                      │
└──────────────────────────────────────────────────────┘
```

**Layout:**
- Mobile: 2×2 grid of metric cards.
- Desktop: single row, 4 items evenly spaced.
- Full-width band with contrasting background (e.g., dark or brand-colored).

**Components:**
- 4 metric blocks: large number + small label beneath
- If numbers not available yet, replace entire strip with a single-line proof statement on a colored band.

**Visual guidance:**
- Use a background color that contrasts with both the hero above and the problem section below to create visual separation.
- Numbers should be the largest element (display/heading size). Labels in caption size.
- Optional: subtle count-up animation on scroll-into-view.

**Content hierarchy:**
- Numbers: H2-weight, white or high-contrast
- Labels: caption, slightly muted

**Interaction notes:**
- Optional: numbers animate (count up) when the section enters the viewport.
- No CTA here. Purpose is trust, not action.

---

## Section 4: Problem

```
MOBILE                                 DESKTOP
┌───────────────────────┐    ┌─────────────────────────────────────┐
│   [Eyebrow]           │    │  [Eyebrow]                          │
│   H2 headline         │    │  H2 headline                        │
│                       │    │                                     │
│   ┌─────────────────┐ │    │  ┌──────────┐ ┌──────────┐         │
│   │  Pain card 1    │ │    │  │ Pain 1   │ │ Pain 2   │         │
│   └─────────────────┘ │    │  └──────────┘ └──────────┘         │
│   ┌─────────────────┐ │    │  ┌──────────┐ ┌──────────┐         │
│   │  Pain card 2    │ │    │  │ Pain 3   │ │ Pain 4   │         │
│   └─────────────────┘ │    │  └──────────┘ └──────────┘         │
│   ┌─────────────────┐ │    │                                     │
│   │  Pain card 3    │ │    │  Transition sentence →              │
│   └─────────────────┘ │    └─────────────────────────────────────┘
│   ┌─────────────────┐ │
│   │  Pain card 4    │ │
│   └─────────────────┘ │
│                       │
│   Transition sentence │
└───────────────────────┘
```

**Layout:**
- Mobile: single column, stacked cards.
- Desktop: 2×2 grid of cards.

**Components:**
- Eyebrow text
- H2 headline
- 4 pain-point cards: each has an emoji or icon, a short title (H3/bold), and 1–2 sentence description.
- Transition sentence below the grid (leads into Solution)

**Visual guidance:**
- Cards should feel slightly "negative" — use a warm/neutral background, maybe a subtle red or orange accent on icons to signal frustration.
- Icons: use simple line icons or emoji. Examples: 📱 (WhatsApp chaos), 💸 (chasing payments), 🔍 (no visibility), 🏗️ (unprofessional image).
- Keep cards uniform height. On mobile, stack vertically with 12px gap.

**Content hierarchy:**
- Eyebrow: overline, muted
- H2: section heading
- Card title: H3 or bold body
- Card description: body/small, muted

---

## Section 5: Solution (3 Pillars)

```
MOBILE                                 DESKTOP
┌───────────────────────┐    ┌─────────────────────────────────────────┐
│   H2 headline         │    │  H2 headline                            │
│   Subhead             │    │  Subhead                                │
│                       │    │                                         │
│   ┌─────────────────┐ │    │  ┌───────────┐┌───────────┐┌──────────┐│
│   │  Icon            │ │    │  │  Icon     ││  Icon     ││  Icon    ││
│   │  Pillar 1 title │ │    │  │  Pillar 1 ││  Pillar 2 ││  Pillar 3││
│   │  Description     │ │    │  │  Title    ││  Title    ││  Title   ││
│   │  • Benefit       │ │    │  │  Desc     ││  Desc     ││  Desc    ││
│   │  • Benefit       │ │    │  │  • Ben    ││  • Ben    ││  • Ben   ││
│   │  • Benefit       │ │    │  │  • Ben    ││  • Ben    ││  • Ben   ││
│   └─────────────────┘ │    │  │  • Ben    ││  • Ben    ││  • Ben   ││
│   ┌─────────────────┐ │    │  └───────────┘└───────────┘└──────────┘│
│   │  Pillar 2...    │ │    │                                         │
│   └─────────────────┘ │    │  [microcopy: pagamento é opcional]      │
│   ┌─────────────────┐ │    │                                         │
│   │  Pillar 3...    │ │    │  [========= CTA =========]              │
│   └─────────────────┘ │    └─────────────────────────────────────────┘
│                       │
│   microcopy           │
│   [===== CTA =====]   │
└───────────────────────┘
```

**Layout:**
- Mobile: single column, 3 stacked cards.
- Desktop: 3-column grid, equal width.

**Components:**
- H2 + subhead
- 3 pillar cards, each containing: icon/illustration, H3 title, 1-paragraph description, 3 benefit bullets
- Microcopy note (about payment being optional)
- Secondary CTA button

**Visual guidance:**
- Each pillar card should have a distinct icon or small illustration at the top. Suggestions: a dumbbell/clipboard (Treinos), a phone screen (App do Aluno), a PIX/money icon (Cobrança).
- Cards should have subtle borders or light background to separate them visually. Same height (use CSS grid or flex stretch).
- Optional: a small app screenshot inside each card showing the relevant feature screen.

**Content hierarchy:**
- H2: section heading
- Subhead: body-large, muted
- Card H3: bold, accent or dark
- Card body: body text
- Bullets: body/small, with checkmark or dot icon
- Microcopy: caption, muted

---

## Section 6: How It Works (2 Columns)

```
MOBILE                                 DESKTOP
┌───────────────────────┐    ┌─────────────────────────────────────────┐
│   H2 headline         │    │           H2 headline                   │
│   Subhead             │    │           Subhead                       │
│                       │    │                                         │
│   [Tab: Personal]     │    │   SEU LADO            │  LADO DO ALUNO  │
│   [Tab: Aluno  ]      │    │                       │                 │
│                       │    │   ① Crie sua conta    │  ① Recebe convite│
│   ① Step 1            │    │      grátis           │     por link    │
│      Description      │    │                       │                 │
│   ② Step 2            │    │   ② Monte o treino   │  ② Baixa o app  │
│      Description      │    │      do aluno         │                 │
│   ③ Step 3            │    │                       │                 │
│      Description      │    │   ③ Convide seu      │  ③ Acessa treino│
│   ④ Step 4            │    │      aluno            │     do dia      │
│      Description      │    │                       │                 │
│                       │    │   ④ Ative cobrança   │  ④ Treina e     │
│                       │    │      (opcional)        │     registra    │
└───────────────────────┘    └─────────────────────────────────────────┘
```

**Layout:**
- Mobile: tabbed interface. Two tabs ("Seu lado" / "Lado do aluno"). Each tab shows 4 vertical steps.
- Desktop: 2-column side-by-side. Divider line or visual separator between columns.

**Components:**
- H2 + subhead
- 2-column layout (or tabs on mobile)
- 4 steps per column, each with: number badge, step title (bold), 1-line description
- Column headers: "Seu lado" and "Lado do aluno"

**Visual guidance:**
- Use numbered circles (①②③④) with the brand accent color.
- A subtle vertical line connecting the steps on each side (timeline style).
- On desktop, a thin vertical divider between the two columns.
- Steps should align horizontally between columns to show the parallel journey.

**Content hierarchy:**
- H2: section heading
- Column headers: H3 or bold/uppercase label
- Step number: accent circle, small
- Step title: bold body
- Step description: body/small, muted

**Interaction notes:**
- Mobile: tabs switch between Personal and Aluno views. No horizontal scroll.
- Desktop: both columns visible simultaneously.

---

## Section 7: First 30 Days Timeline

```
MOBILE                                 DESKTOP
┌───────────────────────┐    ┌─────────────────────────────────────────┐
│   H2 headline         │    │  H2 headline                            │
│   Subhead             │    │  Subhead                                │
│                       │    │                                         │
│   ● Dia 1             │    │  ●───────●───────●───────●───────●      │
│   │ Title             │    │  Dia 1   Sem 1   Sem 2   Sem 3   Dia 30│
│   │ Description       │    │                                         │
│   │                   │    │  [Expanded card for selected milestone]  │
│   ● Semana 1          │    │                                         │
│   │ Title             │    └─────────────────────────────────────────┘
│   │ Description       │
│   │                   │
│   ● Semana 2          │
│   │ Title             │
│   │ Description       │
│   │                   │
│   ● Semana 3          │
│   │ Title             │
│   │ Description       │
│   │                   │
│   ● Dia 30            │
│     Title             │
│     Description       │
└───────────────────────┘
```

**Layout:**
- Mobile: vertical timeline with left-aligned line and dots.
- Desktop: horizontal timeline with dots/steps across the top and an expanded card below showing the active milestone detail. Or, alternatively, the same vertical layout centered.

**Components:**
- H2 + subhead
- 5 milestone nodes: Dia 1, Semana 1, Semana 2, Semana 3, Dia 30
- Each node: dot/marker, time label, title, 1–2 sentence description.

**Visual guidance:**
- Use a connecting line between dots (vertical on mobile, horizontal on desktop).
- Active/completed dots in brand color. Future dots in muted gray.
- On desktop: consider showing all milestones expanded, or use a horizontal stepper where hovering reveals the detail.
- The timeline should feel motivating. Use subtle green/success-colored progress indicators.

**Content hierarchy:**
- H2: section heading
- Time label: overline/caption, bold, muted
- Milestone title: H3 or bold body
- Description: body/small

---

## Section 8: Testimonials

```
MOBILE                                 DESKTOP
┌───────────────────────┐    ┌─────────────────────────────────────────┐
│   H2 headline         │    │           H2 headline                   │
│   Subhead             │    │           Subhead                       │
│                       │    │                                         │
│   ┌─────────────────┐ │    │  ┌───────────┐ ┌───────────┐ ┌────────┐│
│   │  "Quote..."     │ │    │  │ "Quote.." │ │ "Quote.." │ │"Quote."││
│   │                 │ │    │  │           │ │           │ │        ││
│   │  Photo  Name    │ │    │  │ Photo Name│ │ Photo Name│ │Pho Name││
│   │         @handle │ │    │  │    @handle│ │    @handle│ │  @handl││
│   │         City    │ │    │  │    City   │ │    City   │ │  City  ││
│   └─────────────────┘ │    │  └───────────┘ └───────────┘ └────────┘│
│                       │    │                                         │
│   ← [carousel dots] →│    └─────────────────────────────────────────┘
└───────────────────────┘
```

**Layout:**
- Mobile: horizontal carousel (swipeable), 1 card visible at a time, pagination dots below.
- Desktop: 3-column grid, all 3 cards visible.

**Components:**
- H2 + subhead
- 3 testimonial cards: quote text, author photo placeholder (circle), name, handle/social link, city/state
- Mobile: carousel dots + swipe gesture

**Visual guidance:**
- Cards with open quotation mark icon (") at top-left.
- Author photo as 48px circle, left-aligned beside name and meta.
- Soft card background (light gray or white with border).
- Subtle star rating (5 stars) above or below the quote is optional.

**Content hierarchy:**
- H2: section heading
- Quote: body, italic or regular, dark
- Name: bold body
- Meta (handle, city): caption, muted

**Interaction notes:**
- Mobile: swipeable carousel with momentum. Dots indicate position.
- Desktop: static 3-column grid.

---

## Section 9: Pricing

```
MOBILE                                    DESKTOP
┌───────────────────────────┐    ┌──────────────────────────────────────────────┐
│   H2 headline             │    │            H2 headline                       │
│   Subhead                 │    │            Subhead                           │
│                           │    │                                              │
│   ┌─────────────────────┐ │    │  ┌───────────┐ ┌═══════════╗ ┌───────────┐  │
│   ║ ★ BADGE: Popular    ║ │    │  │           │ ║ ★ Popular ║ │           │  │
│   ║                     ║ │    │  │  Pro      │ ║           ║ │  Business │  │
│   ║   GRÁTIS            ║ │    │  │           │ ║  GRÁTIS   ║ │           │  │
│   ║   R$ 0              ║ │    │  │  R$XX/mês │ ║  R$ 0     ║ │  R$XX/mês │  │
│   ║   Até 4 alunos      ║ │    │  │  Até XX   │ ║  Até 4    ║ │  Ilimitado│  │
│   ║                     ║ │    │  │  alunos   │ ║  alunos   ║ │           │  │
│   ║   • Feature         ║ │    │  │           │ ║           ║ │           │  │
│   ║   • Feature         ║ │    │  │  • Feat   │ ║  • Feat   ║ │  • Feat   │  │
│   ║   • Feature         ║ │    │  │  • Feat   │ ║  • Feat   ║ │  • Feat   │  │
│   ║   • Feature         ║ │    │  │  • Feat   │ ║  • Feat   ║ │  • Feat   │  │
│   ║                     ║ │    │  │           │ ║           ║ │           │  │
│   ║   Pra quem é:       ║ │    │  │  Pra quem │ ║  Pra quem ║ │  Pra quem │  │
│   ║   description       ║ │    │  │  é: desc  │ ║  é: desc  ║ │  é: desc  │  │
│   ║                     ║ │    │  │           │ ║           ║ │           │  │
│   ║   [====CTA====]     ║ │    │  │  [ CTA ]  │ ║  [ CTA ]  ║ │  [ CTA ]  │  │
│   ║   microcopy         ║ │    │  │  micro    │ ║  micro    ║ │  micro    │  │
│   ╚═════════════════════╝ │    │  └───────────┘ ╚═══════════╝ └───────────┘  │
│                           │    │                                              │
│   ┌─────────────────────┐ │    │  [footnote about fees]                       │
│   │  Pro card...        │ │    └──────────────────────────────────────────────┘
│   └─────────────────────┘ │
│   ┌─────────────────────┐ │
│   │  Business card...   │ │
│   └─────────────────────┘ │
│                           │
│   footnote about fees     │
└───────────────────────────┘
```

**Layout:**
- Mobile: single column, stacked cards, Grátis first (most prominent).
- Desktop: 3-column grid. Grátis card in the CENTER with a highlighted border/elevation (raised, thicker border, or accent background). Pro left, Business right.

**Components:**
- H2 + subhead
- 3 pricing cards, each with: plan name, badge (on Grátis), price, student limit, 4–5 features, "Pra quem é" description, CTA button, microcopy
- Footnote below all cards (about fees and no hidden costs)

**Visual guidance:**
- Grátis card: slightly elevated (scale: 1.03 or extra shadow), accent-colored border or top bar, "Mais popular" badge.
- Other cards: standard white with light border.
- Use checkmark icons for feature lists.
- "Pra quem é" section: a small italic or muted block at the bottom of each card, separated by a thin line.

**Content hierarchy:**
- Plan name: H3, bold
- Price: display/large number
- Student limit: body, muted
- Features: body/small, with icon
- "Pra quem é": caption/italic
- CTA: primary on Grátis, secondary/outline on others
- Footnote: caption, muted

---

## Section 10: FAQ

```
MOBILE & DESKTOP (same pattern)
┌─────────────────────────────────────────┐
│   H2 headline                           │
│                                         │
│   ┌───────────────────────────────────┐ │
│   │  ▸ Pergunta 1                     │ │
│   └───────────────────────────────────┘ │
│   ┌───────────────────────────────────┐ │
│   │  ▾ Pergunta 2                     │ │
│   │    Resposta text here that        │ │
│   │    expands below the question...  │ │
│   └───────────────────────────────────┘ │
│   ┌───────────────────────────────────┐ │
│   │  ▸ Pergunta 3                     │ │
│   └───────────────────────────────────┘ │
│   ...                                   │
└─────────────────────────────────────────┘
```

**Layout:**
- Same on both breakpoints. Single column, max-width 720px, centered.
- Accordion pattern.

**Components:**
- H2 headline
- 6–8 accordion items: question label (bold) + expand/collapse chevron + answer text

**Visual guidance:**
- Clean and minimal. Light divider lines between items.
- Open state: question bold, answer in body text below, chevron rotates.
- Only one item open at a time (single-expand).
- No background color changes on cards. Keep it simple.

**Content hierarchy:**
- H2: section heading
- Question: bold body
- Answer: body, muted

**Interaction notes:**
- Accordion: click/tap to toggle. Only one answer visible at a time.
- First question open by default on page load.
- Smooth height animation on open/close (200–300ms ease).

---

## Section 11: Final CTA

```
┌─────────────────────────────────────────┐
│                                         │
│          H2 headline                    │
│          Subhead                        │
│                                         │
│          [======= CTA =======]          │
│          microcopy                      │
│                                         │
└─────────────────────────────────────────┘
```

**Layout:**
- Full-width band with contrasting background (brand color or dark).
- All content centered. Single column on all breakpoints.

**Components:**
- H2 headline (white or light text)
- Subhead (1 sentence)
- Primary CTA button (large, contrasting)
- Microcopy (light/muted on dark background)

**Visual guidance:**
- Use brand accent or dark background for strong visual break.
- Big CTA button, minimum 56px height, generous padding.
- This should feel like a "closing statement." Confident, clean, minimal.

---

## Section 12: Footer

```
┌─────────────────────────────────────────────────┐
│                                                 │
│  [Logo]                                         │
│                                                 │
│  Repz          Produto         Legal            │
│  Sobre         Funcionalidades Termos de uso    │
│  Blog          Preços          Privacidade      │
│  Contato       FAQ                              │
│                                                 │
│  ┌─────────────────────────────────────────┐    │
│  │  EM BREVE: Ferramentas de marketing     │    │
│  │  para atrair mais alunos. Acompanhe →   │    │
│  └─────────────────────────────────────────┘    │
│                                                 │
│  [IG] [Social icons]     © 2026 Repz            │
│                                                 │
└─────────────────────────────────────────────────┘
```

**Layout:**
- Mobile: stacked columns (logo, then column groups, then roadmap note, then copyright).
- Desktop: 3–4 column grid with logo above.

**Components:**
- Logo
- 3 link groups: Repz, Produto, Legal
- Roadmap block: small card or highlighted text about upcoming marketing features. Keep it discreet. Use a muted background or subtle border.
- Social media icons
- Copyright line

---
---

# DELIVERABLE 3: UI SYSTEM RECOMMENDATIONS

---

## Grid & Spacing

**Grid:**
- Mobile (360px): 4-column grid, 16px margins, 16px gutter
- Tablet (768px): 8-column grid, 24px margins, 20px gutter
- Desktop (1280px+): 12-column grid, 80px margins (auto-center), 24px gutter
- Max content width: 1200px

**Spacing scale (8px base):**

| Token | Value | Usage |
|-------|-------|-------|
| `space-xs` | 4px | Microcopy gap, inline spacing |
| `space-sm` | 8px | Between related elements (icon + label) |
| `space-md` | 16px | Between cards in mobile stack, paragraph gap |
| `space-lg` | 24px | Between sub-sections, card internal padding |
| `space-xl` | 32px | Between major groups within a section |
| `space-2xl` | 48px | Section top/bottom padding (mobile) |
| `space-3xl` | 64px | Section top/bottom padding (tablet) |
| `space-4xl` | 96px | Section top/bottom padding (desktop) |

**Section rhythm:** Every section uses `space-2xl` vertical padding on mobile, scaling to `space-4xl` on desktop. This creates consistent visual breathing room.

---

## Typography Scale

**Font recommendation:** Inter (free, excellent PT-BR rendering, highly legible on mobile). Alternative: DM Sans for a slightly warmer feel.

| Token | Mobile | Desktop | Weight | Usage |
|-------|--------|---------|--------|-------|
| `display` | 36px / 1.15 | 56px / 1.1 | 700 | Hero H1 only |
| `h2` | 28px / 1.2 | 40px / 1.15 | 700 | Section headings |
| `h3` | 20px / 1.3 | 24px / 1.25 | 600 | Card titles, step labels |
| `body-lg` | 18px / 1.5 | 20px / 1.5 | 400 | Subheads, lead text |
| `body` | 16px / 1.5 | 16px / 1.5 | 400 | Paragraphs, descriptions |
| `body-sm` | 14px / 1.5 | 14px / 1.5 | 400 | Bullets, secondary text |
| `caption` | 12px / 1.4 | 12px / 1.4 | 400 | Microcopy, labels, metadata |
| `overline` | 12px / 1.4 | 13px / 1.4 | 600 | Eyebrow text, section labels |

**Use `clamp()` for fluid scaling:**
Example for H1: `font-size: clamp(2rem, 5vw, 3.5rem);`

---

## Color System (Suggestions)

| Token | Suggested Value | Usage |
|-------|-----------------|-------|
| `brand-primary` | Brand green/blue (from existing Repz palette) | CTA buttons, active states, accents |
| `brand-primary-dark` | 10% darker | Button hover, links on light bg |
| `text-primary` | #1A1A2E or similar dark | Headings, body text |
| `text-secondary` | #6B7280 | Subheads, muted descriptions |
| `text-muted` | #9CA3AF | Captions, microcopy, metadata |
| `surface-default` | #FFFFFF | Card backgrounds, main bg |
| `surface-subtle` | #F9FAFB | Alternating section backgrounds |
| `surface-accent` | Brand color at 8% opacity | Proof strip, CTA band backgrounds |
| `surface-dark` | #1A1A2E | Footer, final CTA band |
| `border` | #E5E7EB | Card borders, dividers |
| `success` | #22C55E | Success states, checkmarks |
| `error` | #EF4444 | Form errors |
| `warning` | #F59E0B | Warning states |

---

## CTA Hierarchy

**Primary button:**
- Background: `brand-primary`
- Text: white, `body` weight 600
- Height: 48px (mobile), 52px (desktop)
- Border-radius: 12px
- Padding: 16px 32px
- Hover: darken 10%, subtle shadow
- Active: darken 15%
- Full-width on mobile hero, auto-width elsewhere

**Secondary button:**
- Background: transparent
- Border: 2px solid `brand-primary`
- Text: `brand-primary`, weight 600
- Same size as primary
- Hover: `brand-primary` bg at 8% opacity

**Text link CTA:**
- Text: `brand-primary`, weight 500, underline on hover
- Optional arrow suffix: →
- No background or border

---

## Component Set

### 1. Feature/Pillar Card
- Background: `surface-default`
- Border: 1px `border`
- Border-radius: 16px
- Padding: `space-lg`
- Content: icon (48px), H3 title, body paragraph, 3 checkmark bullets
- Shadow: 0 1px 3px rgba(0,0,0,0.04) — subtle

### 2. Pain-Point Card
- Same structure as feature card
- Distinct visual: emoji/icon, H3 title, body description
- Slightly warm/neutral bg (e.g., #FFFBF5 or #FFF5F5) to convey frustration

### 3. Testimonial Card
- Background: `surface-default`
- Border: 1px `border`
- Border-radius: 16px
- Content: open-quote icon, quote text (body, italic optional), divider, author row (photo circle 48px, name bold, meta caption)
- Min-height on desktop to align cards

### 4. Pricing Card
- Background: `surface-default`
- Border: 1px `border` (2px `brand-primary` for highlighted plan)
- Border-radius: 16px
- Content: badge pill (conditional), plan name H3, price display, student limit body, feature list with checkmarks, "Pra quem é" caption block, CTA button, microcopy caption
- Highlighted card: slight scale-up (`transform: scale(1.02)`), accent top border or full accent border, shadow increase

### 5. Pill Badge
- Background: `brand-primary` at 12% opacity
- Text: `brand-primary`, `caption` size, weight 600
- Padding: 4px 12px
- Border-radius: 100px (full round)
- Usage: hero eyebrow, pricing "Mais popular" badge

### 6. Proof Metric Block
- Large number: `h2` weight
- Label: `caption`
- Layout: stacked vertically, centered

### 7. FAQ Accordion Item
- Border-bottom: 1px `border`
- Question: `body` weight 600, padding 16px 0
- Chevron: 20px icon, right-aligned
- Answer: `body` weight 400, `text-secondary`, padding-bottom 16px
- Transition: height 250ms ease, chevron rotate 180deg

### 8. Step/Timeline Node
- Circle marker: 32px, `brand-primary` bg, white number inside
- Connecting line: 2px, `border` color
- Content next to marker: H3 title, body description

---

## Accessibility Notes

**Contrast:**
- All text meets WCAG 2.1 AA minimum. Body text on white: at least 4.5:1. Large text (H1/H2): at least 3:1.
- CTA buttons: text on brand-color background must meet 4.5:1. Test with WebAIM contrast checker.
- Microcopy (caption size on light bg): ensure `text-muted` is dark enough. #9CA3AF on white = 3.0:1 — this may fail for small text. Consider darkening to #6B7280 for caption-sized text.

**Touch targets:**
- All tappable elements: minimum 44×44px tap area (following Apple HIG and WCAG 2.5.8).
- Buttons: already 48px+ height. Ensure nav links have enough padding on mobile.
- FAQ accordion items: full-width tap zone, not just the chevron.

**Focus states:**
- All interactive elements must have a visible focus ring: 2px solid `brand-primary`, 2px offset.
- Tab order follows visual order (no layout-breaking tab jumps).
- Skip-to-content link hidden by default, visible on focus.

**Motion:**
- All animations should respect `prefers-reduced-motion`. Replace slide/fade/count-up with instant transitions.
- Carousel auto-play: disabled by default. User controls only.

**Semantics:**
- One `<h1>` per page (hero headline). All section headings are `<h2>`. Sub-items are `<h3>`.
- FAQ uses `<details>/<summary>` or proper ARIA accordion pattern (role="region", aria-expanded).
- Images: all illustrative images have descriptive alt text. Decorative icons use `aria-hidden="true"`.
- Language: `<html lang="pt-BR">`.

---
---

# DELIVERABLE 4: FINAL COPY (PT-BR)

---

## Section 1: Header

**Logo:** Repz

**Nav links:** Funcionalidades · Preços · FAQ

**CTA button:** Criar conta grátis

**Microcopy (desktop only, below CTA):** Sem cartão. Pronto em 2 min.

---

## Section 2: Hero — Variação A

**Eyebrow pill:**
> Para personal trainers que levam o negócio a sério

**H1:**
> Entregue uma consultoria premium.
> Sem perder tempo com planilha e cobrança.

**Subhead:**
> O Repz reúne prescrição de treino, app exclusivo para o aluno e cobrança automática via PIX em um só lugar. Para você focar no que importa: o resultado do seu aluno.

**Bullets:**
- ✅ Monte treinos profissionais em minutos
- ✅ Seu aluno acompanha tudo pelo app, sem grupo de WhatsApp
- ✅ Receba via PIX com cobrança recorrente automática

**CTA primário:** Começar grátis agora

**CTA secundário:** Ver como funciona ↓

**Microcopy:** Grátis até 4 alunos · Sem cartão de crédito · Cancele quando quiser

---

## Section 2: Hero — Variação B

**Eyebrow pill:**
> Chega de improvisar a gestão da sua consultoria

**H1:**
> Pare de mandar treino por WhatsApp
> e de correr atrás de pagamento.

**Subhead:**
> O Repz organiza seus treinos, entrega tudo no app do aluno e cobra automaticamente via PIX. Você ganha tempo, profissionalismo e previsibilidade financeira.

**Bullets:**
- ✅ Treinos personalizados com envio direto pelo app
- ✅ Aluno com acesso próprio (adeus prints e PDFs)
- ✅ Cobrança recorrente no PIX: sem boleto, sem constrangimento

**CTA primário:** Testar grátis agora

**CTA secundário:** Veja o que muda nos seus primeiros 30 dias ↓

**Microcopy:** Grátis até 4 alunos · Sem cartão · Pronto em 2 minutos

---

## Section 3: Proof Strip

**Opção A (com números):**

| Número | Legenda |
|--------|---------|
| [X]+ | Personais ativos |
| [X]+ | Treinos entregues |
| [X]+ | Alunos acompanhados |
| 4.8 ★ | Avaliação no app |

**Opção B (sem números ainda):**
> Usado por personal trainers em todo o Brasil para organizar treinos, encantar alunos e receber em dia.

---

## Section 4: Problema

**Eyebrow:** Você se reconhece?

**H2:** O dia a dia do personal não devia ser assim.

**Card 1 — Treino por WhatsApp e PDF**
> Você monta treino no Word, manda print no grupo e torce pra ninguém se perder. O aluno salva, esquece, e te pergunta tudo de novo.

**Card 2 — Cobrança manual**
> No fim do mês, você vira cobrador: manda PIX, espera, manda de novo. Alguns pagam atrasado. Outros somem.

**Card 3 — Zero visibilidade**
> Você não sabe se o aluno treinou, se tá evoluindo ou se vai cancelar semana que vem.

**Card 4 — Imagem improvisada**
> Enquanto isso, o personal da academia ao lado já tem app próprio e parece uma empresa de verdade.

**Frase de transição:**
> E se existisse um jeito de resolver tudo isso com uma única ferramenta?

---

## Section 5: Solução em 3 Pilares

**H2:** Uma plataforma. Três problemas resolvidos.

**Subhead:** O Repz cuida da prescrição, da entrega e da cobrança. Você cuida do aluno.

---

**Pilar 1: Treinos profissionais**

**H3:** Monte treinos com cara de app premium

> Crie programas personalizados com exercícios, séries, repetições, descanso e observações. Tudo organizado, visual e fácil de atualizar. Seu aluno recebe na hora, direto no app.

- Biblioteca de exercícios pronta para usar
- Copie e adapte treinos entre alunos
- Atualize em tempo real, sem reenviar nada

---

**Pilar 2: App exclusivo do aluno**

**H3:** Seu aluno com tudo na palma da mão

> O aluno abre o app e encontra o treino do dia, histórico de evolução e comunicação direta com você. Sem grupo de WhatsApp, sem PDF perdido, sem dúvida no vácuo.

- Treino do dia com timer e instruções
- Histórico completo de treinos realizados
- Canal direto com o personal pelo app

---

**Pilar 3: Pagamento automático (PIX)**

**H3:** Receba no dia certo. Sem cobrar ninguém.

> Configure a cobrança recorrente via PIX e o Repz cuida do resto. O aluno recebe o lembrete, paga pelo app e você acompanha tudo em um painel financeiro simples.

- Cobrança recorrente automática via PIX
- Painel com status de cada pagamento
- Taxa transparente, sem surpresa [verificar condições atuais]

**Microcopy:** Pagamento automático é opcional. Use só os treinos se preferir.

**CTA:** Criar conta grátis

---

## Section 6: Como Funciona

**H2:** Simples para você. Simples para o aluno.

**Subhead:** Veja o caminho de cada um em poucos passos.

**Coluna: Seu lado**

① **Crie sua conta grátis**
Cadastro rápido, sem cartão. Você já pode começar a montar treinos.

② **Monte o treino do aluno**
Escolha exercícios, defina séries e repetições. Salve e envie.

③ **Convide seu aluno**
O aluno recebe um link, baixa o app e já tem acesso ao treino.

④ **Ative a cobrança (opcional)**
Configure o valor e a recorrência. O Repz cobra automaticamente via PIX.

**Coluna: Lado do aluno**

① **Recebe o convite**
Um link por WhatsApp ou e-mail. Sem formulário longo.

② **Baixa o app**
Disponível para Android e iOS [confirmar disponibilidade].

③ **Acessa o treino do dia**
Abre o app e já vê o que precisa fazer, com instruções e timer.

④ **Treina e registra**
Marca séries feitas, anota cargas e o personal acompanha tudo.

---

## Section 7: Primeiros 30 Dias

**H2:** O que muda nos seus primeiros 30 dias

**Subhead:** Um mês é suficiente para sentir a diferença na rotina e no bolso.

**Dia 1 — Conta criada, primeiro treino montado**
> Em menos de 10 minutos você já tem sua conta e um programa de treino pronto para enviar.

**Semana 1 — Alunos no app, treinos entregues**
> Seus alunos recebem o convite, baixam o app e começam a treinar com acesso direto ao programa.

**Semana 2 — Cobrança automática ativada**
> Configure o PIX recorrente e pare de mandar mensagem cobrando pagamento.

**Semana 3 — Rotina mais leve, visão clara**
> Você acompanha quem treinou, quem pagou e quem precisa de atenção — tudo em um painel.

**Dia 30 — Mais tempo, mais controle, mais profissionalismo**
> Você economizou horas de trabalho administrativo e seus alunos estão tendo uma experiência melhor.

---

## Section 8: Depoimentos

**H2:** Quem usa, recomenda.

**Subhead:** Veja o que outros personal trainers estão falando do Repz.

**Card 1 — Foco: Economia de tempo**
> "[Placeholder: depoimento sobre tempo economizado montando e enviando treinos]"
>
> **[Nome]** · Personal Trainer · @[instagram] · [Cidade/UF]

**Card 2 — Foco: Profissionalismo percebido**
> "[Placeholder: depoimento sobre como o app elevou a percepção de profissionalismo junto aos alunos]"
>
> **[Nome]** · Personal Trainer · @[instagram] · [Cidade/UF]

**Card 3 — Foco: Pagamento em dia**
> "[Placeholder: depoimento sobre como a cobrança automática reduziu inadimplência e constrangimento]"
>
> **[Nome]** · Personal Trainer · @[instagram] · [Cidade/UF]

---

## Section 9: Preços

**H2:** Comece grátis. Cresça no seu ritmo.

**Subhead:** Sem surpresa, sem taxa escondida, sem cartão para testar.

---

**Plano Grátis** ⭐ DESTAQUE

**Badge:** Mais popular para começar
**Preço:** R$ 0
**Limite:** Até 4 alunos

**Inclui:**
- Prescrição de treinos completa
- App do aluno (Android e iOS)
- Cobrança via PIX (taxa por transação)
- Suporte por e-mail

**Pra quem é:**
> Para o personal que está começando ou quer testar sem compromisso.

**CTA:** Criar conta grátis
**Microcopy:** Sem cartão de crédito. Sem prazo de teste.

---

**Plano Pro**

**Preço:** R$ [XX]/mês
**Limite:** Até [XX] alunos

**Inclui:**
- Tudo do plano Grátis
- [Funcionalidades adicionais — definir com produto]
- Suporte prioritário

**Pra quem é:**
> Para o personal que já tem carteira ativa e quer escalar com organização.

**CTA:** Começar com o Pro

---

**Plano Business**

**Preço:** R$ [XX]/mês
**Limite:** Alunos ilimitados

**Inclui:**
- Tudo do plano Pro
- [Funcionalidades premium — definir com produto]
- Suporte dedicado

**Pra quem é:**
> Para estúdios, equipes de personal trainers e consultorias de alto volume.

**CTA:** Falar com o time

---

**Nota de rodapé da seção:**
> Todos os planos incluem cobrança automática via PIX. Taxa por transação igual em todos os planos. Sem fidelidade. [Consulte condições atuais]

---

## Section 10: FAQ

**H2:** Perguntas frequentes

**1. Preciso pagar alguma coisa para começar?**
Não. O plano Grátis permite até 4 alunos, sem custo mensal e sem cartão de crédito. Use por tempo indeterminado.

**2. Meu aluno precisa pagar para usar o app?**
Não. O app do aluno é gratuito. Ele só paga a mensalidade que você define para a consultoria.

**3. Como funciona a cobrança automática via PIX?**
Você define o valor e a data. O Repz envia um lembrete automático para o aluno com o link de pagamento. Quando o aluno paga, o valor cai na sua conta com uma taxa por transação. [Consulte condições atuais]

**4. Sou obrigado a usar a cobrança automática?**
Não. O módulo de pagamento é opcional. Você pode usar o Repz apenas para montar e enviar treinos.

**5. Meus alunos vão conseguir usar o app sozinhos?**
Sim. O app é simples e intuitivo. O aluno recebe um link de convite, cria a conta em segundos e já encontra o treino pronto.

**6. Consigo migrar meus alunos de outro app ou planilha?**
Sim. Cadastre seus alunos manualmente ou peça ajuda ao nosso suporte para migração em volume. [Confirmar disponibilidade de importação em massa]

**7. Funciona para consultoria online e presencial?**
Sim. O treino fica disponível no app independente de onde o aluno treina. Funciona para presencial, online ou híbrido.

**8. Meus dados e dos meus alunos estão seguros?**
Sim. Usamos criptografia e boas práticas de segurança para proteger todas as informações. [Adicionar link para política de privacidade]

---

## Section 11: CTA Final

**H2:** Pronto para profissionalizar sua consultoria?

**Subhead:** Crie sua conta em 2 minutos. Monte seu primeiro treino hoje. Grátis até 4 alunos.

**CTA:** Criar minha conta grátis

**Microcopy:** Sem cartão · Sem compromisso · Suporte incluso

---

## Section 12: Footer

**Coluna 1 — Repz:** Sobre · Blog · Contato

**Coluna 2 — Produto:** Funcionalidades · Preços · FAQ

**Coluna 3 — Legal:** Termos de uso · Política de privacidade

**Bloco Roadmap (discreto):**
> Em breve no Repz: ferramentas de marketing para atrair mais alunos. Acompanhar atualizações →

**Redes:** Instagram · [outras]

**Copyright:** © 2026 Repz. Todos os direitos reservados.

---
---

# DELIVERABLE 5: TWO HERO DESIGN DIRECTIONS

---

## Concept A: "Consultoria premium com menos esforço"

**Positioning:** Aspirational. Speaks to trainers who want to level up their professional image.
**Emotional driver:** Pride, ambition, differentiation.

**H1:** Entregue uma consultoria premium. Sem perder tempo com planilha e cobrança.

**Visual direction:**
- Clean, premium aesthetic. White/light background with subtle brand-color accents.
- Hero image: a polished 3D phone mockup showing the Repz trainer dashboard with a clean workout card visible. The mockup floats on the right side with a soft shadow.
- Optional: a second smaller phone behind/beside it showing the student app view, creating a "two-sides-of-the-platform" visual.
- Feeling: calm confidence. Think Notion or Linear marketing — minimal, smart, premium.

**CTA microcopy:** Grátis até 4 alunos · Sem cartão de crédito · Cancele quando quiser

**Supporting detail:**
- Eyebrow uses a pill badge in brand accent color.
- Bullets use green checkmarks.
- CTA button in solid brand color, secondary is a text link.
- Ample whitespace. Let the headline breathe.

**Best for:** Organic traffic, referral visitors, trainers already considering a tool upgrade.

---

## Concept B: "Chega de WhatsApp e planilha"

**Positioning:** Pain-driven. Speaks directly to the daily frustration of improvised operations.
**Emotional driver:** Relief, frustration, "finally someone gets it."

**H1:** Pare de mandar treino por WhatsApp e de correr atrás de pagamento.

**Visual direction:**
- Slightly more energetic. Could use a light warm background (soft yellow or beige) or keep white with bolder accent elements.
- Hero image: a split visual. LEFT side shows the "before" chaos (blurred/stylized WhatsApp screenshot, messy spreadsheet, PIX QR code floating). RIGHT side shows the Repz app screen — clean, organized, professional. Visual metaphor: messy → clean.
- Alternative: a photo of a personal trainer looking relaxed/smiling at their phone with the Repz interface visible on-screen.
- Feeling: relatable relief. "We know what you're going through, and here's the fix."

**CTA microcopy:** Grátis até 4 alunos · Sem cartão · Pronto em 2 minutos

**Supporting detail:**
- Eyebrow is more conversational: "Chega de improvisar a gestão da sua consultoria."
- Bullets highlight pain removal ("adeus prints e PDFs").
- CTA uses slightly more urgent language: "Testar grátis agora."
- Visual contrast between "before chaos" and "after clarity" reinforces the message.

**Best for:** Paid ads (Meta/Google), cold traffic, trainers actively frustrated with their current setup.

---

## A/B Test Recommendation

Run both concepts with equal traffic for 2–4 weeks. Primary metric: signup conversion rate. Secondary: scroll depth and time-on-page.

Hypothesis: **Concept B will win on cold/paid traffic** (higher identification with pain). **Concept A will win on organic/referral traffic** (aspiration over frustration for warmer audiences).

After the test, consider: use Concept B for paid landing pages and Concept A for the main site accessed via organic search and referrals.

---
---

# APPENDIX: IMPLEMENTATION NOTES

1. **Placeholders flagged with [brackets]** need validation with the product/business team before launch. Search the document for `[` to find all of them.

2. **Proof Strip numbers:** Prioritize getting real data here. Even modest numbers (e.g., "200+ personais ativos") are more effective than no numbers. If real data isn't available at launch, use the single-line proof statement.

3. **Testimonials:** Start collecting immediately using this framework:
   - "Qual era seu maior problema antes do Repz?"
   - "O que mudou depois que começou a usar?"
   - "O que você diria para um colega que ainda não conhece?"
   Video testimonials (30s) are 2–3x more effective than text.

4. **Performance:** Hero image should be optimized (WebP, responsive srcset). Target LCP under 2.5s. Lazy-load everything below the fold.

5. **Analytics events to track:**
   - `hero_cta_click` (with variant A or B)
   - `sticky_cta_click`
   - `pricing_cta_click` (with plan tier)
   - `final_cta_click`
   - `faq_item_expand` (with question index)
   - `scroll_depth` (25%, 50%, 75%, 100%)

6. **Roadmap mention:** The "Marketing — em breve" content exists ONLY in the footer roadmap block. It does not appear as a main feature or pillar anywhere in the primary content flow.
