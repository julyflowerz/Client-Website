# Client Commission Website

A clean Bootstrap website for collecting custom website requests, sending submissions to your email, and linking to 50% deposit payment options.

## Files

- `index.html` — main website page
- `styles.css` — custom styling
- `app.js` — language selector, translations, and form submission logic

## How to run in VS Code

1. Open this folder in VS Code.
2. Install the VS Code extension called **Live Server**.
3. Right-click `index.html`.
4. Click **Open with Live Server**.

## How to connect the form to your email

This starter uses Formspree because a static HTML site on Vercel cannot securely send email by itself.

1. Go to Formspree and create a free account.
2. Create a new form.
3. Copy your form endpoint. It will look like:
   `https://formspree.io/f/abcxyz`
4. In `index.html`, find this line:

```html
<form id="websiteRequestForm" class="application-form" action="https://formspree.io/f/YOUR_FORMSPREE_ID" method="POST">
```

5. Replace `https://formspree.io/f/YOUR_FORMSPREE_ID` with your real endpoint.
6. Submit the form once locally and confirm your email if Formspree asks you to.

## How to set up payments

Use Stripe Payment Links so you do not handle credit/debit card information yourself.

Recommended setup:
- Starter Website full price: $500
  - 50% deposit link: $250
  - Final payment link: $250
- Standard Website full price: $1,000
  - 50% deposit link: $500
  - Final payment link: $500
- Custom Website:
  - Send a custom Stripe invoice or payment link after reviewing the application.

In `index.html`, replace these placeholder links:

```html
https://buy.stripe.com/REPLACE_WITH_YOUR_STARTER_DEPOSIT_LINK
https://buy.stripe.com/REPLACE_WITH_YOUR_STANDARD_DEPOSIT_LINK
```

## How to deploy on Vercel

Option A: GitHub + Vercel

1. Create a new GitHub repo.
2. Upload/push these files.
3. Go to Vercel.
4. Click **Add New Project**.
5. Import your GitHub repo.
6. Deploy.

Option B: Vercel CLI

1. Install Node.js.
2. Open terminal in this project folder.
3. Run:

```bash
npm i -g vercel
vercel --prod
```

## Important business note

For deposits, make sure your page and payment description clearly says:

"50% non-refundable deposit. Remaining 50% due after client approval and before final delivery or launch."

This is not legal advice. For real client work, consider using a short contract or written agreement.
