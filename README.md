# Supply planning explainers

Two self-contained, scroll-driven HTML presentations for buyers and planners:

| File | Topic |
|---|---|
| `supply-resilience.html` | A daily supply resilience ranking: which parts would hurt most if supply stopped, why the ranking can be trusted, and what to do |
| `procurement-planning.html` | A procurement planning simulator: from a forecast change to the exact orders needed, without touching SAP |
| `index.html` | Landing page linking both |

All names and figures are illustrative and do not come from a real company.

## Host on GitHub Pages

1. Create a repository and upload these files to its root.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

## Embed in a Celonis Studio View

Add an **iframe** component and set its URL to one of:

- `https://<your-username>.github.io/<repository-name>/supply-resilience.html`
- `https://<your-username>.github.io/<repository-name>/procurement-planning.html`

Give the component a height of at least about 700 px. GitHub Pages does not block framing.

To switch between both in one iframe, set the URL to
`https://<your-username>.github.io/<repository-name>/$(presentation)` and map an Input dropdown with the two file names to a string View variable called `presentation`.

## Dependencies

Each page is a single HTML file. It loads the Poppins font (Google Fonts) and GSAP 3.12.5 + ScrollTrigger (jsDelivr) from CDNs. Without them, the content stays fully readable, just without animation.
