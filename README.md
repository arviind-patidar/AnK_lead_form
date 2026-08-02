# acre&key Lead Form & HubSpot CRM Integration

An enterprise-grade, accessible, responsive lead-capture modal component built for **acre&key** with Vanilla JavaScript, HTML5, and scoped CSS.

## Features

- 🟠 **Direct HubSpot CRM Integration**: Out-of-the-box submission to HubSpot CRM via official HubSpot Forms API v3 or Webhooks (Zapier, Make, n8n).
- 🌍 **195+ Countries Support**: Interactive country selector with search and mobile bottom-sheet UI.
- 📱 **Smart Phone Input**: Automatic dial-code detection when pasting numbers with international format (`+91...`, `+1...`).
- ⚡ **Auto UTM & Click Tracking**: Captures `utm_source`, `utm_medium`, `utm_campaign`, `utm_term`, `utm_content`, `gclid`, `fclid`, and referral source URL.
- 🛡️ **Anti-Spam & Bot Protection**: Includes hidden honeypot validation, submission time tracking, and cooldown timer session lock.
- ♿ **Accessibility & Keyboard Navigation**: Full WCAG compliance with focus trapping, ARIA attributes, Esc key close, and keyboard-navigable country dropdown.

---

## How to Connect to HubSpot CRM

You can connect your form submissions directly to HubSpot CRM in **2 easy ways**:

### Option 1: Direct HubSpot Forms API (Recommended - No Backend Required)

1. Log into your **HubSpot CRM** account.
2. Navigate to **Marketing > Forms** and create or select a Form containing **First Name**, **Email**, and **Phone / Mobile Phone**.
3. Copy your **HubSpot Portal ID** (Hub ID in top right corner of HubSpot) and **Form GUID** (found in the form embed code / URL).
4. Add the following script configuration before loading `form.js` (or in `<head>`):

```html
<script>
  window.lfHubspotPortalId = "12345678"; // Replace with your HubSpot Hub/Portal ID
  window.lfHubspotFormGuid = "a1b2c3d4-e5f6-7890-abcd-ef1234567890"; // Replace with your HubSpot Form GUID
  window.lfRedirectUrl     = "/thank-you/"; // Optional thank you page URL
</script>
<script src="js/form.js"></script>
```

When a visitor submits the form, leads automatically land as **Contacts in HubSpot CRM** with full email, phone, name, source URL, and tracking data!

---

### Option 2: HubSpot Integration via Zapier / Make / Webhook

If you process leads through Zapier, Make.com, or a webhook endpoint before pushing to HubSpot:

```html
<script>
  window.lfWebhookUrl  = "https://hooks.zapier.com/hooks/catch/YOUR_ZAPIER_ID"; // Your Webhook URL
  window.lfRedirectUrl = "/thank-you/";
</script>
<script src="script.js"></script>
```

---

## File Structure

```
AnK Form/
├── index.html          # Acre & Key landing page showcasing the lead form modal
├── ank-lead-form.html  # Standalone single-file embed snippet (HTML + CSS + JS)
├── css/
│   └── style.css       # Acre & Key design system styles
├── js/
│   └── form.js        # Form controller & HubSpot API submission logic
└── README.md
```
