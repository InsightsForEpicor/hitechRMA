# Hi Tech Auto Parts 3 — RMA Portal

Customer-facing printable Return Merchandise Authorization (RMA) form.

## What it includes
- Company name — required
- Purchase date
- Original invoice number
- Payment method
- Credit-card indicator plus last 4 digits only
- Configurable **Add Card Information Securely** link
- Part number — required
- Quantity and amount charged
- Multiple part lines
- Optional contact, phone, email, return reason, PO/reference and notes
- Automatically generated RMA number
- Print-friendly RMA sheet
- Local reprint lookup on the same browser/device

## Credit-card security
Do **not** collect full card numbers, CVV, or expiration dates directly in this static GitHub Pages form.

In `index.html`, set:

```js
const CONFIG = {
  secureCardUrl: "https://YOUR-PCI-COMPLIANT-CARD-FORM"
};
```

Use a PCI-compliant processor or secure hosted form.

## Important: tracking
The current static GitHub Pages version generates a unique RMA number and lets a customer reprint an RMA stored on the same browser.

True cross-device customer tracking such as **Received → Inspecting → Approved → Credited** requires a shared backend/database. A good next step is to connect the site to Netlify Functions / Supabase or another secure database, then add an employee/admin status screen.

## Publish with GitHub Pages
Repository: `InsightsForEpicor/hitechRMA`

In GitHub:
1. Open **Settings**
2. Open **Pages**
3. Under **Build and deployment**, select **Deploy from a branch**
4. Select `main` and `/(root)`
5. Save

The page should then be available from the repository's GitHub Pages URL.
