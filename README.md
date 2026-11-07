# AlgoWise Technologies - Website

A single-file static website (HTML, CSS, JavaScript). No build step needed.

## Files
- `index.html` - the entire website, including the logo (embedded) and all styles/scripts.

## Edit
Open `index.html` in any code editor (VS Code recommended) and use Find (Ctrl+F):
- **Prices, tiers, add-ons:** search `var T={` (Websites, Mobile apps, AI solutions, Care plans). Each tier row is:
  `[badge, name, who it is for, [features], list price, founding price, timeline, flag]`
  (flag `1` = Recommended card, `'from'` = shows "From").
- **Industry packs:** search `var IN=`.
- **Services cards:** search `var SV=`.
- **Bundles, offer banner (20%), FAQ, leadership, footer:** search the visible text, e.g. `Founding client offer`.
- **Phone / email / website:** search `var CFG=` and change the 4 values once. The contact box, WhatsApp button and email options all use them.
- **Tab icon:** the AlgoWise icon is embedded in the `<link rel="icon">` line in the head; `favicon.svg` is the same icon as a separate file.
- **Country list for phone numbers:** search `var CC=`.
- **Colours:** edit the variables at the top of the `<style>` block (`--gold`, `--dk`, `--bg`).

Preview locally by double-clicking `index.html` (needs internet for fonts and the 3D engine).

## Deploy on Vercel (free)
**Option A: drag and drop**
1. Go to https://vercel.com/new and sign in.
2. Upload this folder (or push it to GitHub and import the repo).
3. Framework preset: **Other**. Build command: leave empty. Output directory: leave empty (root).
4. Deploy. Add a custom domain under Project > Settings > Domains.

**Option B: Vercel CLI**
```
npm i -g vercel
cd algowise-website
vercel --prod
```

Other hosts that work the same way: Netlify (drag the folder to app.netlify.com/drop), GitHub Pages, Cloudflare Pages.

## Notes
- The contact form validates name, mobile (by country), email and details before sending. WhatsApp opens with the message pre-filled; email offers Gmail, Outlook, the default mail app, or Copy message. For a stored-enquiries inbox, connect a form service (e.g. Formspree, Web3Forms) later.
- Prices exclude 18% GST. Update the validity date (31 March 2027) when the offer changes.
