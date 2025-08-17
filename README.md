
# Modern Register Form (HTML + CSS)

Glassmorphic signup card with floating labels and neon gradient button.

## Structure
```text
modern-register/
├─ index.html
└─ style.css
```

## Quick Start
1. Save the provided HTML as `index.html` and the CSS as `style.css`.
2. Keep these in `<head>`:
```html
<link rel="stylesheet" href="style.css"/>
<link href="https://fonts.googleapis.com/css2?family=Vazirmatn&display=swap" rel="stylesheet" />
```
3. Open `index.html` in a browser.

## Fixes (apply in your CSS)
```css
/* typo: use rgba, not rgbe */
.register-form{ background: rgba(255,255,255,0.05); }

/* animation name + keyframes corrected */
.form-wrapper{ animation: slideIn 1.2s ease forwards; }
@keyframes slideIn{
  from{ transform: translateY(80px); opacity: 0; }
  to  { transform: translateY(0);   opacity: 1; }
}
```

## Customize
- **Colors:** adjust page gradient in `body` and button gradient in `button`.
- **Blur/Glass:** tweak `backdrop-filter` on `.register-form`.
- **Card size:** change `.register-form { width: 320px; padding: 40px 30px; }`.
- **Label behavior:** edit `.input-group input:focus + label, .input-group input:valid + label`.

## Troubleshooting
- **Labels don’t float?** Ensure inputs have `required` or a value so `:valid` triggers.
- **No blur?** `backdrop-filter` needs browser support; provide opaque background as fallback.
- **Font not loading?** Verify the Google Fonts link.

