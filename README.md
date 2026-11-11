# Sundayblues — four-page fashion website

A responsive HTML/CSS/JavaScript student project for GitHub Pages and Google Analytics 4.

## Files
- `index.html` — Home
- `products.html` — Product collection and category filters
- `about.html` — Brand story, mission, vision and sample testimonials
- `contact.html` — Demo enquiry and newsletter forms
- `style.css` — Shared responsive styling
- `script.js` — Mobile menu, filters, validation and GA4 events

## Run locally
Open `index.html` in a browser. For a more reliable local preview, use the VS Code Live Server extension. Keep all six files in the same folder.

## Before publishing
In all four HTML files, replace both occurrences of `G-XXXXXXXXXX` in the Google tag with your actual GA4 Measurement ID. The sample forms do not send or store data. They fire `demo_form_submit` after successful browser validation. Product buttons fire `select_item`.

## Images
The page uses publicly accessible Unsplash image URLs. An internet connection is required for those images and Google Fonts to load. If an image URL changes, replace it with another image URL or a local file path such as `images/your-image.jpg`.

## GitHub Pages
Create a public repository, upload the six files (and the `images` folder if you add local images) to the repository root, then go to Settings → Pages. Under Build and deployment, choose Deploy from a branch, select `main` and `/ (root)`, and save. Your site will be published at `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/` (allow a few minutes).

## Google Analytics 4
1. Go to https://analytics.google.com/ and create an account/property.
2. Add a Web data stream for your published GitHub Pages URL.
3. Copy the Measurement ID beginning `G-`.
4. Replace `G-XXXXXXXXXX` in the Google tag in the `<head>` of all four HTML files.
5. Commit and push the changes. Check Reports → Realtime after visiting your site.
6. Use Google Tag Assistant / GA4 DebugView for debugging. DebugView may require enabling debug mode via Tag Assistant or a supported debugging setup.

## Events included
- `select_item`: product button clicks, with item information.
- `demo_form_submit`: valid contact form or newsletter demo submission.
No `generate_lead` or `sign_up` event is sent because these demo forms do not actually deliver an enquiry or register a subscriber. If you later connect a real form service and confirm successful delivery/registration, update the success callback to send `generate_lead` or `sign_up` only after the service confirms success.

## Important
Prices, products, contact details, testimonials and the brand are illustrative. This is not a functioning ecommerce store.
