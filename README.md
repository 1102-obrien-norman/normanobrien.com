# normanobrien.com

Personal site for Norman O'Brien: SEO & GEO consulting, projects, and background.

Plain HTML and CSS, with no build step or framework. Hosted free on GitHub Pages, with the domain registered at Namecheap.

## What's in this folder

| File | What it does |
|---|---|
| `index.html` | The whole site (content, styles, and a little JavaScript for the hero animation) |
| `404.html` | Page shown for broken links |
| `favicon.svg` | The browser tab icon |
| `headshot.jpg` | Your photo (you add this; see "Headshot tips") |
| `og-image.png` | Preview image shown when the link is shared on LinkedIn, iMessage, Slack, etc. |
| `robots.txt` | Tells search engines and AI crawlers they're allowed to read the site |
| `sitemap.xml` | List of pages for Google Search Console and Bing Webmaster Tools |
| `llms.txt` | A plain-text summary of the site for AI systems (an emerging GEO convention) |
| `CNAME` | Tells GitHub Pages to serve the site at normanobrien.com |

## Before you publish: edit these

Search `index.html` for `EDIT:` to find each spot.

- **Headshot:** add a photo named exactly `headshot.jpg` to this folder (see below). Until you do, your initials show in its place.
- Email address (`hello@normanobrien.com`; see step 6 below to make it work for free)
- The tool's name, once you pick one (it's currently called "AI visibility tracker")
- Specifics for your capstone (data source, methods, results)
- What you did at the Michael J. Fox Foundation
- Graduation year, if it isn't 2027
- If you change your email or name, also update `llms.txt`

### Headshot tips

- **Square crop**, face centered, with some space above your head. The site shows it as a circle.
- **About 600 × 600 pixels and under 200 KB.** Big photos slow the page down, and speed counts for SEO. squoosh.app is a free tool that resizes and compresses in your browser.
- A plain or softly blurred background, good natural light, and a collared shirt or whatever you'd wear to meet a client.
- Use the same photo as LinkedIn so people recognize you across both.

---

## Getting it online for the least money

**Total cost: just the domain.** Hosting on GitHub Pages is free, and HTTPS (the padlock) is free.

### 1. Buy the domain on Namecheap

1. Search for `normanobrien.com` on namecheap.com and add it to your cart for **1 year**.
2. At checkout, **skip every add-on**: hosting, Premium DNS, SSL certificates, and Professional Email. You don't need any of them for this setup.
3. Make sure domain privacy is on (it's free at Namecheap) so your home address isn't public.
4. After purchase, turn on **auto-renew** so you never lose the domain.

### 2. Create a GitHub account and repository

1. Sign up at github.com. Pick a professional username, since it'll also appear on your resume.
2. Click **New repository**. Name it `normanobrien.com` (any name works). Set it to **Public** (Pages is free for public repos).
3. On the empty repo page, click **uploading an existing file**, drag in **everything in this folder** (including `CNAME`), and click **Commit changes**.

No command line is required. You can edit files right on github.com later.

### 3. Turn on GitHub Pages

1. In the repo, go to **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
3. Under **Custom domain**, enter `normanobrien.com` and **Save**. (The `CNAME` file should fill this in automatically.)
4. Recommended: verify the domain so no one else can claim it. Go to your **profile Settings → Pages → Add a domain**. GitHub gives you a TXT record to add in Namecheap (next step).

### 4. Point the domain at GitHub (Namecheap DNS)

In Namecheap, go to **Domain List → Manage (next to normanobrien.com) → Advanced DNS**.

1. **Delete** the default parking records Namecheap adds (usually a `CNAME www → parkingpage.namecheap.com` and a `URL Redirect @` record).
2. Add these records:

| Type | Host | Value |
|---|---|---|
| A Record | `@` | `185.199.108.153` |
| A Record | `@` | `185.199.109.153` |
| A Record | `@` | `185.199.110.153` |
| A Record | `@` | `185.199.111.153` |
| CNAME Record | `www` | `YOUR-GITHUB-USERNAME.github.io.` |
| TXT Record | (from GitHub's verify step) | (from GitHub's verify step) |

Leave TTL on Automatic. Replace `YOUR-GITHUB-USERNAME` with your actual username.

### 5. Wait, then turn on HTTPS

DNS changes take anywhere from a few minutes to about a day. Once the Pages settings screen shows a green "DNS check successful", tick **Enforce HTTPS**. (If the box is greyed out, GitHub is still issuing the certificate. Check back in an hour.)

Visit https://normanobrien.com. `www.normanobrien.com` will redirect to it automatically.

### 6. Free email at your domain (optional, recommended)

A `hello@normanobrien.com` address looks much more professional to clients than a Gmail.

1. In Namecheap **Advanced DNS**, under **Mail Settings**, choose **Email Forwarding**.
2. On the **Domain** tab, find **Redirect Email** and add `hello` → your personal Gmail.

Mail sent to hello@normanobrien.com now lands in your Gmail. (To *reply* from that address you can set up Gmail's "Send mail as", or keep replying from Gmail.)

### 7. Get indexed (practice what you preach)

1. **Google Search Console** (search.google.com/search-console): add `normanobrien.com` as a **Domain** property, verify with the TXT record it gives you (add it in Namecheap), then submit `https://normanobrien.com/sitemap.xml`.
2. **Bing Webmaster Tools** (bing.com/webmasters): you can import straight from Search Console. Bing's index also feeds some AI assistants, so it matters for GEO.
3. Put the link on your LinkedIn (Contact info → Website, and in your Featured section), GitHub profile, and resume.

---

## Updating the site later

Open the file on github.com, click the pencil icon, make your change, and click **Commit changes**. The live site updates in about a minute. When you add pages, add them to `sitemap.xml` too.

## Costs at a glance

| Item | Cost |
|---|---|
| Domain (.com at Namecheap) | First year often discounted with a promo. Namecheap's regular .com prices from Nov 1, 2026 are $15.98 to register and $19.98/yr to renew, plus a $0.20 ICANN fee. |
| Hosting (GitHub Pages) | Free |
| HTTPS certificate | Free (automatic) |
| Email forwarding | Free |
