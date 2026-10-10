# Digital Growth Hub

A responsive, static agency website built with HTML, CSS, and vanilla JavaScript. Open `index.html` in a browser; there is no build step or framework requirement.

## Pages

Home, About, Services, Team, Work, Pricing, Testimonials, Resources, Contact, Privacy Policy (draft), Terms & Conditions (draft), and five sample article pages are provided. The article content, concept work, team details, and testimonials are clearly labeled as samples or placeholders.

## Configure business details and integrations

Edit [`assets/js/config.js`](assets/js/config.js). Add the real business email, WhatsApp number in international digits-only format, LinkedIn and Instagram URLs, optional team profile data, and public booking URL when available. Team photos and social links only appear when public HTTPS URLs are supplied. Leave a setting blank to keep its link or control hidden. Add the public HTTPS form and newsletter endpoints to `formEndpoint` and `newsletterEndpoint` when ready. Endpoints must accept `FormData` POST requests and return a successful HTTP response only after confirming receipt. The browser code contains no secret keys; configure credentials and spam protection on the server.

Set `currency` and `budgets` in the same file to customize the contact form budget choices. The contact and newsletter forms clearly report preview mode and do not claim delivery until a configured endpoint confirms success.

## Update content

Pages are standalone HTML documents sharing `assets/css/styles.css` and `assets/js/main.js`. Update the repeated navigation and footer in each HTML page when changing site-wide links. `scripts/generate_pages.ps1` is the page generation source used for this initial version; from the project root, run `powershell -NoProfile -ExecutionPolicy Bypass -File .\scripts\generate_pages.ps1` to regenerate the pages. Review generated content before publishing, especially legal drafts and sample editorial content.

## Before publishing

- Replace placeholders with verified company, team, and contact information.
- Review the draft Privacy Policy and Terms & Conditions for the actual business and jurisdiction.
- Review sample articles before publication and configure a real article author if needed.
- Configure and test secure form endpoints, newsletter handling, spam controls, WhatsApp, and booking links.
- Replace generic social destinations with the agency’s actual profiles.

## Technical notes

The site uses CSS Grid and Flexbox, inline CSS-built concept visuals, accessible menu/accordion controls, working portfolio filters and resource search, keyboard focus styles, responsive layouts, and reduced-motion support. Google Fonts are optional; system font fallbacks are included. Scroll reveals use IntersectionObserver and content stays visible when JavaScript is unavailable.
