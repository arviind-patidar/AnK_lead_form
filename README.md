# AnK Lead Form

An enterprise-grade, accessible, responsive lead-capture modal component built with Vanilla JavaScript, HTML5, and scoped CSS.

## Features

- 🌍 **195+ Countries Support**: Interactive country selector with search and mobile bottom-sheet UI.
- 📱 **Smart Phone Input**: Automatic dial-code detection when pasting numbers with international format (`+91...`, `+1...`).
- ⚡ **Auto UTM & Click Tracking**: Captures `utm_source`, `utm_medium`, `utm_campaign`, `utm_term`, `utm_content`, `gclid`, `fclid`, and referral source URL.
- 🛡️ **Anti-Spam & Bot Protection**: Includes hidden honeypot validation, submission time tracking, and cooldown timer session lock.
- ♿ **Accessibility & Keyboard Navigation**: Full WCAG compliance with focus trapping, ARIA attributes, Esc key close, and keyboard-navigable country dropdown.
- 🎨 **WordPress & Webflow Compatible**: Isolated `.lf-` CSS class names to prevent style leakage on existing websites.

## File Structure

```
AnK Form/
├── index.html          # Demo landing page showcasing the lead form modal
├── ank-lead-form.html  # Standalone single-file embed snippet (HTML + CSS + JS)
├── css/
│   └── style.css       # Form modal & demo page styles
├── js/
│   └── form.js        # Form controller logic & validation
└── README.md
```

## Configuration

Set the following configuration variables before loading `form.js` or directly inside the script block:

```javascript
window.lfWebhookUrl  = "https://your-api-endpoint.com/lead-webhook"; // Destination webhook URL
window.lfRedirectUrl = "/thank-you/";                              // Post-submit redirect page
window.lfFormSecret  = "YOUR_OPTIONAL_API_KEY";                   // Sent as X-Form-Secret header
```

## Setup & Deployment

### Option A: Standard Web App Integration

1. Link `css/style.css` in your document `<head>`:
   ```html
   <link rel="stylesheet" href="css/style.css">
   ```
2. Include the CTA trigger button and modal markup from `index.html`.
3. Load `js/form.js` before `</body>`:
   ```html
   <script src="js/form.js"></script>
   ```

### Option B: WordPress / Webflow HTML Embed

Copy the contents of `ank-lead-form.html` directly into your WordPress HTML Block or Webflow Embed Component. Remember to replace `"https://YOUR_WEBHOOK_URL_HERE"` with your actual webhook receiver URL.
