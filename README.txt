SHOP EASY UTC-ELGON — setup guide

FILES
- index.html: complete mobile-friendly storefront and admin UI
- schema.sql: creates shared product table and basic access policies

IMPORTANT SECURITY NOTE
This starter uses Supabase Auth for the admin login. The SQL allows any authenticated Supabase user to manage products, so before production use, turn off public sign-ups in Supabase Authentication settings and create only the trusted admin user(s). Never put a Supabase service_role/secret key in index.html. Only use the publishable/anon key in the browser.

SETUP
1. Create a Supabase project at https://supabase.com/ and save its Project URL and publishable/anon key.
2. In Supabase, open SQL Editor, paste schema.sql, and run it.
3. In Supabase Authentication settings, disable public sign-ups. Create your admin user from Authentication > Users (or the supported invite flow), and use that email/password in the site's Admin sign-in.
4. Open index.html and replace YOUR_SUPABASE_PROJECT_URL and YOUR_SUPABASE_PUBLISHABLE_OR_ANON_KEY with your Supabase Project URL and publishable/anon key. Never use a service_role/secret key.
5. Create a GitHub repository named shop-easy-utce. Upload index.html and schema.sql to the repository root.
6. In Netlify, choose Add new project > Import an existing project > GitHub, select shop-easy-utce, set build command blank and publish directory . (repository root), then deploy.
7. Open the deployed site and test the Admin login, add a test product, then check the public shop from a private/incognito browser. Tap Order on WhatsApp and confirm the message goes to 256753443115.

IMAGE NOTES
Use publicly accessible https:// image URLs for product photos. Do not use private drive links. Product images can be hosted using Supabase Storage or another public image host.

WHATSAPP
The order links are configured for 256753443115. WhatsApp opens with product name, price, ID, and quantity prefilled. The customer must tap Send; the website does not automatically send messages or process payments.
