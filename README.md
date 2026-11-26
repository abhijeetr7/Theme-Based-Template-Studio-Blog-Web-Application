ThemeCraft Studio — Composable Theme & Template Blog Web Application

Live Demo: https://abhijeetr7.github.io/Theme-Based-Template-Studio-Blog-Web-Application/

Overview & Purpose

ThemeCraft Studio is a zero-build, single-file Composable Page Builder, Theme Engine, and JSON-Driven Blog Application built with pure HTML, CSS Custom Properties, Tailwind CSS utilities, and vanilla JavaScript.

Modern headless publishing platforms often receive dynamic content feeds whose structure or field names aren't known in advance. ThemeCraft solves this by completely decoupling Visual Aesthetics (Themes), Page Composition & Structure (Blueprints), and Dynamic Content (Schema-Agnostic JSON Feeds)—empowering administrators to design, preview, and publish entirely different user experiences in real time without touching source code.

Core Capabilities

1. Three-Mode Studio Workspace

Reader View: The live, user-facing publication styled by the currently published theme and page blueprint, complete with category filtering, live search, interactive carousels, sequential series tracks, and a full-article reading modal.

Composable Page Builder: A 3-pane visual blueprint studio featuring a component inspector on the left, a multi-viewport interactive canvas (Desktop 100%, Tablet 768px, Mobile 375px) in the center, and a live Blueprint JSON & Scoped CSS editor on the right.

Admin Dashboard: A centralized control center for managing themes, page blueprints, content entries, external JSON ingestion, and full JSON state export/import.

2. Full-Page Composable Architecture (Header → Middle Sequence → Footer)

Administrators can assemble custom page blueprints from top to bottom:

Header Section Customizer (headerConfig):

Switch between Editorial Masthead, Top Nav + Search, Accent Hero Banner, and Compact Minimal styles.

Control masthead alignment (left, center, split) and toggle category navigation pills, live search bars, or publication taglines.

Middle Content Sequence Builder (sections[]):

Stack, reorder (↑ / ↓), configure columns/card surfaces, or remove any ordered sequence of content blocks rendered immediately after the header:

Interactive Hero Carousel (carousel): Interactive slider with dot pagination, slide counter (1 / N), and previous/next controls.

Blog Cards by Series / Sequence (series-tracks): Automatically groups incoming JSON items by their series (or category fallback) and sorts them numerically by sequence / episode number (#01, #02, #03...).

Single Spotlight Hero (spotlight-hero): Full-width featured story banner.

Direct Blog Cards Grid (post-grid): Responsive 1-to-4 column article cards (elevated, bordered, glass, minimal-line, or flat).

Release Timeline (changelog-timeline): Vertical timeline with milestone dots and version badges.

Numbered Digest List (newsletter-digest): Scannable, numbered issue rows with read-time badges.

Portfolio Visual Cards (portfolio-grid): Full-bleed cover photography with dark gradient overlays and metric badges.

Feed + Sticky Sidebar (split-sidebar): Main editorial feed paired with a sticky publication summary sidebar.

Footer Section Customizer (footerConfig):

Choose between Multi-Column Links (auto-populated with active topics and series), Newsletter CTA + Bar, Single Line Bar, or Hidden.

3. Dynamic CSS Token Theme Engine

Switch between 4 curated built-in themes (Editorial Serif, Midnight Cyber, Minimalist Nordic, Warm Terracotta) or create custom themes.

Live-edit CSS custom properties (--bg-primary, --bg-surface, --text-primary, --primary-color, --accent-color, --radius, and heading/body font pairings) with instant visual feedback across all layout blueprints.

4. Schema-Agnostic JSON Feed Ingestor

Designed to render unknown external JSON payloads seamlessly.

Automatically normalizes arbitrary JSON keys (such as headline, seriesName, episode, summary, topic, creator, or img) into unified content models without breaking layouts.

Includes a ⚡ Test External JSON simulator inside the Page Builder and a Dynamic JSON Feed Ingestor inside the Admin Dashboard.

5. Draft-to-Publish Workflow & JSON Portability

All edits in the Admin Dashboard and Page Builder happen safely in a Draft State with a real-time browser preview.

Click Publish to Reader View to push changes live and persist them in localStorage.

Export or import the entire application state as blog-config.json.

JSON Blueprint Schema Example

{
  "id": "carousel-series-blueprint",
  "name": "Carousel + Series Sequences",
  "containerWidth": "standard",
  "headerConfig": {
    "style": "navbar",
    "align": "left",
    "showNav": true,
    "showSearch": true,
    "showTagline": true
  },
  "sections": [
    {
      "id": "sec-carousel-1",
      "type": "carousel",
      "title": "Featured Highlights",
      "maxItems": 3,
      "cardStyle": "elevated"
    },
    {
      "id": "sec-series-1",
      "type": "series-tracks",
      "title": "Curated Series & Learning Sequences",
      "columns": 3,
      "cardStyle": "bordered"
    }
  ],
  "footerConfig": {
    "style": "columns",
    "showBadges": true
  }
}


Getting Started

Try it Online: Open the Live Demo.

Run Locally: Because the entire application is self-contained in index.html, simply clone the repository and open index.html in any modern web browser—no Node.js, bundlers, or build steps required.

git clone https://github.com/abhijeetr7/Theme-Based-Template-Studio-Blog-Web-Application.git
cd Theme-Based-Template-Studio-Blog-Web-Application
# Open index.html in your browser
