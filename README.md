# LINKER FAIZAN

Instagram ബയോയ്ക്കുള്ള ലിങ്ക് പേജ് മേക്കർ. Cloudflare Workers + KV.

## ഫയലുകൾ
- `_worker.js` : ഫോം, പേജ്, SEO, ഐക്കൺ, സെർവർ കോഡ് എല്ലാം ഇതിലുണ്ട്
- `wrangler.jsonc` : Cloudflare-ന് ഏത് ഫയൽ ഓടിക്കണം, KV (`LINKS`) എന്നിവ പറയുന്നു
- `icons/` : ആപ്പ് ഐക്കൺ (SVG, PNG 1024/512/192)

## ഡിപ്ലോയ്
1. ഈ ഫയലുകൾ GitHub repo-യിൽ ഇടുക (`_worker.js`, `wrangler.jsonc`, `README.md` എന്നിവ repo-യുടെ ഏറ്റവും മുകളിൽ).
2. Cloudflare Worker-നെ ഈ repo-യുമായി ബന്ധിപ്പിക്കുക.
3. `wrangler.jsonc`-ലെ `name` Worker പേരുമായി ഒത്തുപോകണം.

## ഉപയോഗം
Worker ലിങ്ക് തുറന്ന് പേര്, ലിങ്ക് പേര്, പാസ്‌വേഡ് നൽകി സേവ് ചെയ്യുക.
പേജ് `സൈറ്റ്/ലിങ്ക്-പേര്` ആയിരിക്കും. എഡിറ്റ് ചെയ്യാൻ പേജിലെ "എഡിറ്റ്" അമർത്തി പാസ്‌വേഡ് നൽകുക.


## Google Search Console Verification
- Verification path: `/googlefbc46c776af9c892.html`
- The Cloudflare Worker serves the exact Google verification response at this path. A matching HTML file is also included in the ZIP.
- Deploy the updated Worker, then open `https://YOUR-DOMAIN/googlefbc46c776af9c892.html` and confirm it displays `google-site-verification: googlefbc46c776af9c892.html`.
- In Google Search Console, select HTML file verification and press **Verify**. Keep this route in the Worker after verification.


## Animated icon update
- The logo beside LINKER FAIZAN now gently floats and glows inside the app.
- The installed Android/PWA home-screen icon remains static; Android PWA launcher icons do not support animation.
- Animation automatically stops when the device requests reduced motion.
