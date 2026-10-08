[README.md](https://github.com/user-attachments/files/33223705/README.md)
# Nicole Backal — portfolio site

A single self-contained page. No build step, no dependencies, no framework. You edit
`index.html` in any text editor and the site changes.

```
portfolio/
├── index.html      ← the whole site
├── images/         ← put your photos here
└── README.md       ← this file
```

---

## Adding your photos

1. Pick six photos to start with.
2. Resize each to about **1600px on the long edge** and save as JPEG, quality ~80.
   Anything bigger just makes the page slow — nobody views a portfolio at full resolution.
   On a Mac you can do all six at once: select them in Finder → right-click →
   *Quick Actions* → *Convert Image* → Medium.
3. Name them exactly `photo-01.jpg`, `photo-02.jpg` … `photo-06.jpg`.
4. Drop them into the `images/` folder.
5. Open `index.html`, find the Photography section, and replace each
   `Caption — place, year` with a real caption.

A tile whose file is missing shows a labeled placeholder instead of a broken image, so
you can add them one at a time without the page looking unfinished.

**To add more than six:** copy one `<li class="photo">` block, paste it below the last
one, and bump the filename to `photo-07.jpg`. Also update the `06` in the section
heading.

**To use a different aspect ratio:** in the `<style>` block find `.frame` and change
`aspect-ratio: 4/5` — `1/1` for square, `3/2` for landscape.

---

## Publishing it

### GitHub Pages — free, gives you `nicolebackals.github.io`

1. Create a GitHub account if you don't have one, then create a new **public**
   repository named exactly `nicolebackals.github.io` (substitute your username).
2. On the repo page click **Add file → Upload files**, drag in `index.html` and the
   `images` folder, and commit.
3. Go to **Settings → Pages**. Under *Branch* pick `main` and `/ (root)`, then save.
4. Wait two or three minutes. Your site is live at `https://nicolebackals.github.io`.

To update it later, upload the changed file again — it overwrites.

### Netlify — free, easier, gives you a random name you can change

1. Go to netlify.com and sign up.
2. Drag the whole `portfolio` folder onto the deploy area on your dashboard.
3. It's live immediately at something like `cheerful-pastry-12ab.netlify.app`.
4. **Site configuration → Change site name** to make it `nicolebackal.netlify.app`.

Netlify is faster to set up; GitHub Pages gives you a cleaner-looking free URL. Either
one accepts a custom domain later.

### Your own domain

A `.com` runs about $12/year from Namecheap or Cloudflare. Both hosts above have a
*Custom domain* setting that walks you through pointing it. `nicolebackal.com` is worth
owning before someone else takes it.

---

## Things to fix before you send this to anyone

- **Writing section** points at a Student Life *search* URL. Replace it with a direct
  link to one specific article.
- **Roles in the Film & Video list** are guesses. Correct any that are wrong.
- **Runtimes** aren't listed. Add them (`Director · Short Film · 8 min`) — people decide
  whether to click based on length.
- **LinkedIn** isn't linked anywhere. Add it to the Contact section when you have one.

Your phone number is deliberately not on this page. A résumé goes to one recruiter; a
website is indexed by Google and scraped by everyone. Email is enough.

---

## Editing notes

Everything is commented. The section you want is marked with a `<!-- ... -->` block
above it.

Colors and fonts live in the `:root` block at the top of the `<style>` section. Change
a value there and it updates everywhere. The page already has a dark mode that follows
the visitor's system setting — if you change a color, change its dark counterpart in
the two blocks below `:root` as well.
