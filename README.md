# GHL embeds

## Carpen CFO

App URL: https://carpen-cfo-lwhxnn2q.manus.space

### Option A: sidebar menu link (inside the GHL app)
1. Go to **Agency Settings → Custom Menu Links** (or **Settings → Custom Menu Links** in a sub-account).
2. Click **Create New**.
3. Title: `Carpen CFO`, URL: `https://carpen-cfo-lwhxnn2q.manus.space`
4. Open mode: **iFrame inside the application**.
5. Pick which sub-accounts or users can see it, then save.

### Option B: funnel or website page
1. Open the page in the Funnel/Website builder.
2. Add a **Custom JS/HTML** element to a full-width section.
3. Paste the contents of [`embeds/carpen-cfo-iframe.html`](embeds/carpen-cfo-iframe.html) and save.

### If the frame shows up blank
The app has to allow framing. If the browser console shows `Refused to display ... in a frame`,
the Manus site is sending `X-Frame-Options` or a `Content-Security-Policy: frame-ancestors` header.
Allow `*.gohighlevel.com`, `*.leadconnectorhq.com` and your white-label/custom domain in that
header, or use the "Open in new tab" mode for the custom menu link instead.
