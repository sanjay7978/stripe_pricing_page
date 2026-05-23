stripe_pricing_elite.html — README
What it is
A Stripe-style pricing page — a polished, self-contained HTML component with 3 plan cards (Starter, Growth, Scale) plus an Enterprise contact row.
Features
UI & Layout

Dark hero section with gradient mesh background and animated dot-pulse badge
3-column card grid: Starter (free), Growth ($49/mo, featured), Scale ($149/mo)
Monthly / Annual billing toggle with animated price transitions — annual pricing shows 20% savings
Enterprise strip at the bottom for custom contracts

Interactivity

Billing toggle switches prices with a spring animation (cubic-bezier easing)
Cards have hover lift effects with box-shadow transitions
Buttons use sendPrompt() — meaning they're wired to fire chat messages (designed to work inside a Claude artifact or similar chat-embedded context)

Trust bar at the bottom: SOC 2 Type II · Encrypted at rest · 14-day trial · No card required · Cancel anytime
Plan Summary
PlanMonthlyAnnualHighlightsStarterFreeFree3 projects, 5 GB, community supportGrowth$49/seat$39/seatUnlimited projects, 100 GB, 10 seatsScale$149/seat$119/seatUnlimited everything, 2 TB, 99.99% SLAEnterpriseCustomCustomDedicated infra, SOC 2, custom contracts
Tech Stack

Pure HTML + CSS + vanilla JS (no framework, no dependencies)
Google Fonts: Inter
Icons: Tabler Icons via CDN (ti ti-* classes)
Uses CSS custom properties (--accent, --ink, etc.) for easy theming
