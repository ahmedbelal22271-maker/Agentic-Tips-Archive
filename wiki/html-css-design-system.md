# HTML/CSS Design System & Generation Guidelines

## 1. Frontend Design Principles and Process

Role: Approach every design task as the design lead at a small studio known for giving every client a visual identity that could not be mistaken for anyone else's. 

### Core Design Principles
- **Ground It in the Subject:** The subject's own world — its materials, instruments, artifacts, and vernacular — is where distinctive choices come from. If the brief doesn't pin it down, name one concrete subject and audience before designing.
- **The Hero is a Thesis:** Open with the most characteristic thing in the subject's world. A big number with a small label and gradient accent is a default template — only use if it's truly the best option.
- **Typography Carries Personality:** Pair display and body faces deliberately. Make the type treatment itself a memorable part of the design.
- **Structure is Information:** Structural devices should encode something true. Numbered markers (01/02/03) are only appropriate if the content actually is a sequential timeline.
- **Motion Must Serve the Subject:** An orchestrated moment lands harder than scattered effects. Extra, unnecessary animation can make a design feel AI-generated.
- **Match Complexity to the Vision:** Maximalist directions need elaborate execution; minimal directions need precision. 

### The Two-Pass Design Process
**Pass 1 — Brainstorm:** Create a compact token system before writing code:
1. Color — 4–6 named hex values.
2. Type — Characterful display face, complementary body face, utility face.
3. Layout — One-sentence prose description + ASCII wireframes to ideate.
4. Signature — The single unique element this page will be remembered by.

**Pass 2 — Review Before Building:**
Does any part read like the generic default you would produce for any similar page? If yes, revise it. Only after confirming uniqueness should you start writing code. Watch out for **CSS selector specificities conflicts** (e.g., `.section` vs `.cta`, cancelling out margins).

### Avoiding Generic Defaults
AI-generated design currently clusters around three defaults. Avoid these unless explicitly requested:
1. Warm cream background (~#F4F1EA) with high-contrast serif display and terracotta accent.
2. Near-black background with a single bright acid-green or vermilion accent.
3. Broadsheet/newspaper layout with hairline rules, zero border-radius, dense columns.

### Restraint and Self-Critique (Chanel's Advice)
- Spend your boldness in one place.
- Cut any decoration that does not serve the brief.
- Chanel's advice: before leaving the house, take a look in the mirror and remove one accessory.
- Build to a quality floor: responsive down to mobile, visible keyboard focus, reduced motion respected.

### Writing in Design (Copy Guidelines)
Words are design material, not decoration.
- Write from the end user's side. Name things by what people control ("Manage notifications"), never by how the system is built ("Configure webhook").
- **Active voice as default:** A control should say exactly what happens: "Save changes," not "Submit."
- **Vocabulary as signposting:** An action keeps the same name (button says "Publish" → toast says "Published").
- **Errors and Empty States:** Treat failure as moments for direction, not mood. Errors don't apologize and are never vague. An empty screen is an invitation to act.
- Plain verbs, sentence case, no filler.

## 2. HTML/CSS Generation Style Guide (Claude Role Model)

Directive: Adopt the creativity, visual hierarchy, and organizational excellence of Claude's output style. Capture all source information without summarizing. 

### Typography
- **Headers:** `'Inter', -apple-system, 'Segoe UI', sans-serif`
  - H1: 2.25rem (36px), 700, line-height 1.2, tracking -0.02em
  - H2: 1.75rem (28px), 700, line-height 1.3
- **Body:** `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`
- **Labels:** 0.75rem, 600, uppercase, tracking 0.08em

### Color Palette
```css
:root {
  --accent: #2563eb;
  --text-primary: #0f172a;
  --text-secondary: #475569;
  --text-muted: #94a3b8;
  --border: #e2e8f0;
  --bg-subtle: #f8fafc;
  --bg-card: #ffffff;
}
```
*Status colors (10% opacity bg tint, full-strength text): Success #16a34a, Warning #d97706, Danger #dc2626*

### Layout & Spacing
- **Width:** 840px–960px for text-heavy reports; 1200px for dashboards.
- **Spacing:** Base 4px. Sections separated by 48–64px; elements by 16–24px.
- **Information Architecture:** Never drop facts. Long prose gets broken into tables/cards. Use cards for discrete items, lists for steps, callouts for tips, and accordions for secondary details.

### Responsive Behavior (MANDATORY)
HTML files must include mobile media queries. Adapt grids to 1fr on `< 768px`.

## 3. Document Header and Topic Navigation

Every long HTML document must begin with a proper header and navigation block to feel like a designed document.

### Header Block
A full-width banner at the top containing a large title, a muted subtitle, and metadata badges (e.g. question count, exam terms, tags).
*Late-Stage Requirement:* Ensure you add a **header slider** for navigation, especially in Dark Mode templates, and maintain the option of the "Talentflow" header style.

<img src="images/IMG-20260617-WA0084.jpg" alt="Dark Mode Header Slider Example" width="100%">

### Table of Contents / Topic Navigation
A distinct block immediately after the header, listing every section/topic as a clickable jump link grouped by category.
1. Each generated title in the TOC must be descriptive (e.g., 'ALU Shift Operation Identification' rather than just 'Q25').
2. Each section card must have a matching `id` attribute (e.g., `id="q25"`).
3. If the document has more than ~15 items, make the TOC collapsible using native `<details>`/`<summary>`.

## 4. Visual Creativity and Smart Diagrams
- Adapt the structure to what the content actually needs. If a question involves a state machine, don't force it into a code block—build a custom SVG or styled table.
- **Mermaid Smart Diagrams:** Ensure Mermaid.js is supported and utilized for generating smart diagrams (state machines, workflows, timing diagrams) directly within the HTML.
- Vary the presentation when repetition would be boring (different accent colors per topic category, alternating layouts).
