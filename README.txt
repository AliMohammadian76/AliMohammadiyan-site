ALI MOHAMMADIYAN — PERSONAL WEBSITE
====================================

UPLOAD INSTRUCTIONS
-------------------
Upload the contents of this folder to the ROOT of the web hosting
(usually public_html/ or www/), keeping the folder structure exactly:

  /index.html                     <- the whole site (single file)
  /robots.txt
  /sitemap.xml
  /img/og-image.jpg               <- social preview card (1200x630)
  /img/ali-mohammadiyan.jpg       <- portrait, referenced by structured data
  /img/apple-touch-icon.png       <- iOS home-screen icon (180x180)
  /pdf/AliMohammadiyanResume.pdf  <- ADD THIS YOURSELF (see below)

index.html replaces the old homepage. It is fully self-contained:
all CSS is inline and the About photo is embedded as base64, so the
page renders correctly even before the /img/ files are uploaded.
The only external request is Google Fonts.


THINGS TO DO BEFORE / AFTER UPLOAD
----------------------------------
1. CV FILE — create a /pdf/ folder and put the resume there as:
      /pdf/AliMohammadiyanResume.pdf
   The "Download CV" buttons link to that exact path.

2. DOMAIN — every URL in the <head> and in the JSON-LD block is written
   as https://www.alimohammadiyan.com/ . If the site is served WITHOUT
   the "www" prefix (or on another domain), open index.html in a text
   editor and replace every occurrence of
      https://www.alimohammadiyan.com
   with the real address. Affected tags: canonical, og:url, og:image,
   twitter:image, and the JSON-LD "@id"/"url"/"image" fields.

3. HTTPS — make sure the site is served over HTTPS (og:image:secure_url
   requires it, and Google treats HTTP as a negative signal).

4. GOOGLE SEARCH CONSOLE — add the domain, then submit
      https://www.alimohammadiyan.com/sitemap.xml
   Indexing usually takes a few days.

5. LINKEDIN PREVIEW — after upload, paste the URL into
      https://www.linkedin.com/post-inspector/
   This refreshes LinkedIn's cached preview so the og-image card shows.
   Do the same on X with the Card Validator if needed.

6. VERIFY STRUCTURED DATA —
      https://search.google.com/test/rich-results
   Paste the live URL; the Person / ProfilePage / WebSite entities
   should be detected with no errors.


WHAT'S IN THE PAGE
------------------
Sections: Hero -> About -> Skills -> Experience -> Education -> Contact
- Mobile responsive (tested at 390px and 1280px)
- Print stylesheet included (Ctrl+P produces a clean one-pager)
- Accessible: skip link, semantic landmarks, visible focus outlines,
  reduced-motion support
- SEO: title, meta description, robots directives, canonical,
  full Open Graph + Twitter Card set, and JSON-LD structured data

Contact email used throughout: info@alimohammadiyan.com
