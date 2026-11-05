# GHL embeds

## Bright Skies Services funnel (3 steps)

| Step | Path | Paste this file |
| --- | --- | --- |
| 1. Landing page + survey popup | `/` (any path) | [`embeds/brightsky/1-landing.html`](embeds/brightsky/1-landing.html) |
| 2. Booking (Calendly) | `/booking` | [`embeds/brightsky/2-booking.html`](embeds/brightsky/2-booking.html) |
| 3. Confirmation | `/confirmation` | [`embeds/brightsky/3-confirmation.html`](embeds/brightsky/3-confirmation.html) |

For each step:
1. Add a section, set it to **Full Width**, and set the padding of the section, row and column to 0.
2. Add one **Custom JS/HTML** element to it, paste the whole file, and save.
3. Test on the preview or live URL. The builder canvas doesn't run the scripts.

Wiring the steps together:
- **Survey → booking:** in the survey's settings, set the submit action to redirect to the booking step's URL.
- **Booking → confirmation:** handled by the code. When Calendly reports a completed booking, the page
  goes to `/confirmation`. If your step path is different, change `CONFIRMATION_URL` at the top of
  the script in `2-booking.html`, and the `/booking` link in `3-confirmation.html`.
- The confirmation step shows "You're booked!" only after a real booking on step 2. Opening it
  directly shows a neutral "Booking status" message.

Why the popup is built on `<dialog>`: the survey popup opens with the browser's native
`showModal()`. That puts it in the top layer, so GHL's section animations (transforms),
`overflow: hidden` wrappers and sticky headers can't push it off screen or cover it.

## Carpen CFO

App URL: https://carpen-cfo-lwhxnn2q.manus.space

### Funnel or website page
Add a **Custom JS/HTML** element to a full-width section and paste the contents of
[`embeds/carpen-cfo-iframe.html`](embeds/carpen-cfo-iframe.html).

The embed shows the app in a frame with an **Open in new tab** button above it, so the app
is always reachable even if it can't run inside the frame.

### Sidebar menu link
**Settings → Custom Menu Links → Create New**, URL `https://carpen-cfo-lwhxnn2q.manus.space`,
open mode **Open in new tab**.
