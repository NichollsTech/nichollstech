# How to edit your Nicholls Tech website

The whole site is one file: **nicholls-tech-website.html**

To edit it: open it in a plain text editor — **not** Word. On Windows use Notepad (or download the free VS Code / Notepad++). On Mac use TextEdit, but switch it to plain text mode first (Format → Make Plain Text), or download VS Code (free, easier).

After editing, save the file and double-click it (or drag it into a browser) to preview your changes.

Tip: use your editor's **Find** (Ctrl+F / Cmd+F) to jump straight to the markers below instead of scrolling.

---

## 1. Write your own introduction

Search for: `EDIT START: INTRODUCTION`

You'll see this:

```html
<p>Write your introduction here. A couple of paragraphs about who you are...</p>
<p>This is also a good place to mention what makes you different...</p>
```

Replace the text between `<p>` and `</p>` with your own words. Each `<p>...</p>` is one paragraph — add more by copying a whole line, or delete one you don't need. Don't touch the `<p>` and `</p>` parts themselves, just the words in between.

---

## 2. Add or edit gear for hire (Sound / Light)

Search for: `GEAR FOR HIRE` to find the section, then look for `gear-card sound` or `gear-card light`.

Each item looks like this:

```html
<div class="gear-card sound">
  <span class="tag mono">Sound</span>
  <h3>PA System — Small</h3>
  <p class="spec">Powered speakers + subs<br>Suits up to ~100 people</p>
  <div class="rate">From <span>$—</span> / day</div>
</div>
```

- **To edit an item:** just change the text — the name (`<h3>`), the spec lines (`<p class="spec">`, use `<br>` for a line break), and the price (replace `$—`).
- **To add a new item:** select one whole block, from `<div class="gear-card sound">` down to its matching `</div>`, copy it, paste it just above the `add-card` line in the same category, then edit the copy.
- **Sound items** use `gear-card sound`. **Light items** use `gear-card light`. Keep them in their matching section so the colour-coding (blue for sound, amber for light) stays correct.
- **To remove an item:** delete the whole block the same way, from its opening `<div class="gear-card ...">` to its closing `</div>`.

---

## 3. Add photos from gigs

Search for: `Add photo`

Placeholder slots look like this:

```html
<div class="photo-slot empty">Add photo</div>
```

Replace one with:

```html
<div class="photo-slot"><img src="photos/gig1.jpg" alt="Describe the photo"></div>
```

Two ways to point to a photo:
- **A web link** — if the photo is already online (e.g. Instagram, Google Drive share link, your own hosting), put that link inside the quotes after `src=`.
- **A local file** — create a folder called `photos` in the same place as the HTML file, put your images in it, and use `photos/yourfilename.jpg` as shown above (must match the exact filename).

---

## 4. Edit references/testimonials

Search for: `ref-card`. Replace the quote text and the name/event line:

```html
<div class="ref-card">
  <p class="quote">"Add a short quote from a client here..."</p>
  <div class="who">— Name, event / band</div>
</div>
```

Copy a whole `ref-card` block to add another one.

---

## 5. Contact details / footer

Search for: `id="contact"`. Your email, phone, and Instagram link are already filled in there and repeated at the very bottom of the page — update both places if any of them change.

---

## 6. Logo

The logo is currently the circular mark cropped from your business card image. When you send over the clean cutout/transparent PNG, I can drop it straight in at full quality — no need to edit the code yourself for that one.
