# WebEkwal Technologies Website

A responsive, single-page marketing website for WebEkwal Technologies. It introduces the company's digital services, explains its trial and partnership offers, presents pricing, answers common questions, and provides contact options.

## Features

- Responsive layout with desktop navigation and a mobile navigation drawer.
- Service overview for website, web application, and mobile application development, social media management, digital creative services, and ongoing support.
- Three-month trial and 12-month partnership descriptions, including pricing and deliverable terms.
- Pricing plans, a four-step engagement process, and an interactive FAQ accordion.
- WhatsApp and telephone contact links, plus a consultation form interface.
- Floating chat-style assistant with a small, predefined set of local responses.
- Scroll-reveal animations, a first-visit preloader, and reduced-motion styling.

## Technology

- HTML5 for page structure and content.
- Tailwind CSS loaded from its CDN, with an inline Tailwind configuration and custom CSS.
- Vanilla JavaScript for page interactions; there is no build step or package manager configuration.
- Google Fonts (`Inter` and `Space Grotesk`) loaded remotely.

Tailwind CSS and the fonts are loaded from external services, so an internet connection is needed for the intended styling and typography. Without it, the HTML remains available but the page may look different.

## Run Locally

The site is static. Open `mypage/index.html` in a modern browser, or start a local static web server from the `mypage` directory.

For example, with Python installed:

```bash
cd mypage
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Project Structure

```text
.
|-- README.md
`-- mypage/
    `-- index.html   # Complete page markup, styles, and client-side behavior
```

## Important Behavior Notes

- The consultation form validates required fields in the browser, then displays a confirmation toast and resets. It does not send, store, or email form data. Connect it to a backend or a form service before using it to collect real inquiries.
- The chat-style assistant uses hard-coded keyword matching in the browser. It is not connected to an AI model or remote service.
- WhatsApp and telephone links use contact details embedded in `mypage/index.html`. Update them before reusing the page for another business.
- Pricing, offer terms, contact details, and the copyright year are static page content and should be reviewed before publication.
- Domain, hosting, paid API, and advertising costs are described on the page as client-paid external costs.

## Publish as a Website

The project is static and can be hosted on GitHub Pages or another static hosting provider. Since the entry page is inside `mypage/`, configure the hosting workflow to publish that directory, or move the website files to the publishing root if using GitHub Pages' branch-based root publishing option. The README at the repository root is documentation; it is not the website entry page.

For GitHub Pages, open the repository's **Settings** > **Pages**, select the appropriate deployment source, and configure its workflow to upload `mypage/` as the Pages artifact. After deployment, GitHub displays the published URL in the Pages settings.

## Customization

Edit `mypage/index.html` to change page content, branding, pricing, phone and WhatsApp links, colors, or interactions. The Tailwind CDN configuration and custom CSS are near the top of the file; the JavaScript interaction code is near the bottom.

## License

No license is currently specified. Add a license file if you intend to grant permissions for reuse or redistribution.