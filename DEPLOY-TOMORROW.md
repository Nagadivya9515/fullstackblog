# 🚀 TOMORROW — Ship the Blog (30–40 min)

Everything's prepped. Just follow top to bottom.

---

## Part A · Get it live on GitHub Pages (~15 min)

**1. Unzip** `fullstack-blog.zip` somewhere on your machine.
   Inside you have: `index.html`, `images/`, `.nojekyll`.

**2. Create the repo** (this ALSO fixes your 404):
   New repo → name it **exactly** `nagadivya9515.github.io` → Public → Create.

**3. Push it:**
```bash
cd fullstack-blog
git init
git add .
git commit -m "Post 1: How the Web Actually Works"
git branch -M main
git remote add origin https://github.com/Nagadivya9515/nagadivya9515.github.io.git
git push -u origin main
```

**4. Enable Pages:**
   Repo → Settings → Pages → Source: **Deploy from a branch** → `main` / `root` → Save.

**5. Wait ~1 min**, then open **https://nagadivya9515.github.io/** — live. ✅
   (The 404 is gone because the repo name now matches your username.)

---

## Part B · Free domain via Student Pack (~15 min)

**1. Verify (if not already):** https://education.github.com/pack
   Use your Manipal student ID / college email.

**2. Claim a domain** from the Pack → Domains:
   - **Name.com** → free `.dev` / `.app` (a `.dev` reads best for a dev blog), OR
   - **Namecheap** → free `.me`
   → **Turn OFF auto-renew immediately** so you're never charged after year one.

**3. Point DNS** (at the registrar you chose):
   | Type | Host | Value |
   |---|---|---|
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | nagadivya9515.github.io |

**4. Tell GitHub about it:**
   - Add a file named **`CNAME`** (no extension) to the repo, containing just your domain, e.g.:
     ```
     nagadivya.dev
     ```
   - Settings → Pages → Custom domain → enter your domain → Save → tick **Enforce HTTPS**.

**5. Wait for DNS** (10 min–1 hr). Then `https://your-domain.dev` serves the blog. ✅

---

## Part C · Make it look pro on GitHub (~10 min, optional)

- Add the **profile README** (`profile-README.md`) to a repo named `Nagadivya9515`.
- In the blog repo: add a short description + topics (`blog`, `webdev`, `html`).
- Pin the blog repo on your profile.

---

## Notes
- Deploying with the `images/` folder (this package) keeps the page light and cache-friendly — better than the single embedded file for a real site.
- To add **Post 2** later: drop `post2.html` in the repo, link it from `index.html`. When the series grows past 3–4 posts, migrate to **Astro** for a reusable template.
- Google indexing: after it's live, submit the URL in **Google Search Console** to start ranking (matters for the SEO plan).

**Blocker check:** the only thing that needs *you* is the Student Pack verification. If that's already done, the whole thing is ~30 min tomorrow.
