# lofty-demo-scaffold

> A leaner hackathon scaffold for a real-estate SaaS dashboard — CRM, help hub, settings, and a command palette, built with Next.js and Tailwind CSS.

## What It Does

`lofty-demo-scaffold` is the original, stripped-down version of the BrokerDesk / Lofty UI scaffold. It replicates the surface area of a real-estate operating system without the heavier systems (RAG engine, calendar integration, or guide overlays). Use it when you need a fast, believable dashboard shell for demos, hackathons, or UI testing.

### What's Included

- **Marketing Landing Page** — Clean homepage shell.
- **App Shell** — Collapsible sidebar, top nav, utility rail, and breadcrumb chrome.
- **CRM** — Lead pipeline, search, filters, and lead detail views populated with fixture data.
- **AI Copilot Stubs** — Placeholder pages for an AI Assistant, Sales Agent, and Social Agent.
- **Communication** — Inbox, texting, and calling workspace stubs.
- **Automation & Marketplace** — Workflow builder and marketplace browsing placeholders.
- **Transactions** — Transaction roles, checklist templates, and document template pages.
- **Settings** — Profile, account security, notifications, integrations, organization, and vendor settings with working forms.
- **Help Hub** — Docs library, FAQ, glossary, tutorials, and a fuzzy-searchable command palette (`Ctrl+K`).
- **Search** — Nav-route index and static search for the command palette.

## Tech Stack

| Layer | Technology |
|-------|------------|
| Framework | [Next.js](https://nextjs.org/) 15 (App Router, Turbopack) |
| Language | TypeScript |
| Styling | [Tailwind CSS](https://tailwindcss.com/) v4 |
| Icons | [Lucide React](https://lucide.dev/) |
| Font | Inter (Google Fonts) |

## Quick Start

```bash
# Install dependencies
npm install

# Run dev server with Turbopack
npm run dev

# Open http://localhost:3000
```

## Project Structure

```
app/
  page.tsx                 # Marketing landing site
  layout.tsx               # Root layout (Inter font)
  app/                     # Authenticated dashboard
    page.tsx               # Dashboard home
    ai/                    # AI Copilot page stubs
    automation/            # Automation builder stub
    communication/         # Inbox, texting, calling
    content/               # Content stub
    crm/                   # CRM leads & pipeline
    help/                  # Help Hub (docs, FAQ, glossary, tutorials)
    lead-settings/         # Capture, routing, tags, import
    marketing/             # Marketing stub
    marketplace/           # Marketplace stub
    reporting/             # Reporting stub
    sales/                 # Sales stub
    settings/              # Profile, account, notifications, integrations
    transactions/          # Roles, checklists, documents
components/
  app/                     # Dashboard-specific components (CRM, forms)
  help/                    # Command palette, docs, FAQ, glossary, tutorials, Markdown renderer
  shell/                   # AppShell, SideNav, TopNav, UtilityRail, nav config
  ui/                      # Reusable primitives (Button, Card, Input, Tabs, ...)
lib/
  fixtures/                # Demo lead, task, org, user data
  help/                    # Static help content (docs, FAQ, glossary, tutorials)
  search/                  # Nav search index builder
  storage/                 # localStorage abstractions (preferences, progress)
```

## Notable Features

### Command Palette

Press `Ctrl+K` (or `Cmd+K`) to open a fuzzy-searchable palette covering every nav route and help article. It’s built on a static index generated from the nav config and help content.

### Help Content

All docs, FAQs, and tutorials are stored as TypeScript modules in `lib/help/*.content.ts` for fast in-memory rendering with zero CMS dependency.

### Fixture Data

CRM leads, tasks, organizations, and user profiles are hard-coded fixture files. Great for screenshots and demo flows without spinning up a backend.

## Relationship to blistering-barnacles

This is the **lighter predecessor**. If you need the full RAG support engine, in-app guided tours, FullCalendar scheduling, or test suites, see [blistering-barnacles](https://github.com/reuben-roy/blistering-barnacles).

## License

No explicit LICENSE file. Assume all rights reserved unless otherwise stated.

---

Scaffolded with care by [Reuben Roy](https://github.com/reuben-roy).
