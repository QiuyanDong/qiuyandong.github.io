# Ann Dong — Data Science Portfolio

A static site. No build step, no dependencies, no framework. Open any `.html` file in a browser and it works.

---

## Putting it online (about 10 minutes, no command line)

1. Make a GitHub account if you don't have one. Pick the username carefully — it becomes your URL.
2. Create a new repository named exactly **`YOURUSERNAME.github.io`** (your real username, then `.github.io`). Set it to **Public**.
3. On the empty repo page, click **uploading an existing file**.
4. Drag in every file from this folder — all the `.html` files, `style.css`, and the `images` folder. Not the folder itself, the contents.
5. Click **Commit changes**.
6. Wait about a minute, then open `https://YOURUSERNAME.github.io`

That's the URL you submit. If it 404s, give it another two minutes — the first deploy is slow. Check **Settings → Pages** and confirm the source is set to the `main` branch.

To edit later: click any file on GitHub, hit the pencil icon, change the text, commit. Changes appear on the live site in under a minute.

---

## Files

| File | What it is |
|---|---|
| `index.html` | Homepage |
| `about.html` | About |
| `resume.html` | Resume |
| `projects.html` | Project index |
| `project-1.html` | One project write-up — copy this file for each additional project |
| `writing.html` | Writing index |
| `post-1.html` | One post — copy this file for each additional post |
| `contact.html` | Contact |
| `style.css` | All styling for every page |
| `images/` | Your figures and photo go here |

---

## How the layout works

Each content block is a `.row` with two parts:

```html
<section class="row">
  <div class="gutter">   <!-- definitions, captions, metadata -->
  <div class="main">     <!-- the actual prose -->
</section>
```

The left margin is for **real information**: plain-language definitions of specialised terms, figure notes, project metadata. It exists so you can define *Transformer* or *connectome* without breaking the flow of a sentence — which is what your Voice Chart asks for.

An empty `<div class="gutter"></div>` is fine and often correct. Don't invent notes to fill space.

On phones the margin folds underneath the paragraph it belongs to.

---

## Adding an image

Put the file in `images/`, then replace a placeholder block:

```html
<!-- before -->
<figure>
  <div class="figure-empty">Drop your project figure here…</div>
  <figcaption>…</figcaption>
</figure>

<!-- after -->
<figure>
  <img src="images/featured.png" alt="Accuracy by training set size, showing a plateau above 10,000 samples">
  <figcaption>Accuracy plateaus above roughly 10,000 annotated samples.</figcaption>
</figure>
```

Write a real `alt` description — it's what a screen reader announces, and it's checked by accessibility tools.

**Export figures at about 1600 px wide** so they stay sharp on a high-resolution screen.

---

## Before you submit

- [ ] Every yellow-highlighted placeholder is gone. Search the folder for `class="todo"` — zero results means you're clean.
- [ ] Every `[BRACKET]` is gone.
- [ ] Real email, GitHub, and LinkedIn URLs in all page footers (they're currently `example.com`).
- [ ] Resume PDF added to the folder as `Ann_Dong_Resume_2026.pdf`, and the download link works.
- [ ] Opened the live URL on your phone.
- [ ] Clicked every nav link and button.
- [ ] Submitted `https://YOURUSERNAME.github.io` — not a `localhost` or file path.

---

## Design notes, if you're asked

- **Layout:** an annotated page. The margin holds definitions and captions so technical terms get explained without interrupting the argument — the structure does the work your Voice Chart asks the writing to do.
- **Type:** Archivo for headings (heavy grotesk, weight without the compressed poster feel), Newsreader for body (a serif reads as thinking rather than selling, which suits a site whose central section is called *Writing*).
- **Colour:** teal and gold, taken from the legend of the site map — teal for primary sections, gold to mark the core evidence.
- **Images:** none, by default. On a technical portfolio the only images worth having are your own figures. Stock photography quietly announces "template," and an empty slot costs less than a decorative one.
