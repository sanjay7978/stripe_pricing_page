# stripe-pricing-elite

A polished, Stripe inspired pricing page component — pure HTML, CSS, and vanilla JS. No framework, no build step.

## Preview

> Dark hero section · 3-tier card grid · Monthly/Annual billing toggle · Enterprise row · Trust bar

## Plans

| Plan | Monthly | Annual | Key Limits |
|---|---|---|---|
| **Starter** | Free | Free | 3 projects · 5 GB · Community support |
| **Growth** | $49 / seat | $39 / seat | Unlimited projects · 100 GB · Up to 10 seats |
| **Scale** | $149 / seat | $119 / seat | Unlimited everything · 2 TB · 99.99% uptime SLA |
| **Enterprise** | Custom | Custom | Dedicated infra · SOC 2 Type II · Custom contracts |

## Features

- **Billing toggle** — switches between monthly and annual pricing with spring-eased number animations
- **Hover effects** — cards lift with box-shadow transitions on hover
- **Featured card** — Growth plan highlighted with accent border and "Most popular" badge
- **Trust bar** — SOC 2 · Encrypted at rest · 14-day trial · No card required · Cancel anytime
- **`sendPrompt()` hooks** — buttons fire chat messages, ready for Claude artifact or chatbot embedding
- **Accessible** — `aria-hidden` on decorative icons, `sr-only` page heading

## Tech

- Zero dependencies — plain HTML + CSS + JS
- **Icons:** [Tabler Icons](https://tabler.io/icons) via CDN (`ti ti-*`)
- **Font:** [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts
- CSS custom properties for easy theming

## Usage

Just drop the file into your project and open it in a browser:

```bash
# No install needed
open stripe_pricing_elite.html
```

To embed inside a page, wrap the contents in a container div and include the `<style>` and `<script>` blocks.

### Replacing button actions

By default, buttons call `sendPrompt('...')` — a function for chat-embedded contexts. Replace with your own handler:

```js
// Example: redirect to Stripe Checkout
function handlePlanClick(plan) {
  window.location.href = `/checkout?plan=${plan}`;
}
```

Then update each button's `onclick`:

```html
<button class="btn btn-accent" onclick="handlePlanClick('growth')">Start free trial</button>
```

### Theming

All colors are CSS variables in `:root`. Override any of them:

```css
:root {
  --accent: #your-brand-color;
  --green: #your-success-color;
  --ink: #your-text-color;
}
```

## Pricing Logic

Annual prices are hardcoded in the JS object — update them here:

```js
const prices = {
  g:  { m: 49,  a: 39  },   // Growth
  sc: { m: 149, a: 119 }    // Scale
};
```

## License

MIT — use freely in personal and commercial projects.
