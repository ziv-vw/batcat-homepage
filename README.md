# bat-cat.net

The homepage for zii, ziv & ziu — projects, journals, and Tangyuan & Niangao.

## What lives where

- `content.json` — **all the words and photos**: journal entries, projects, gallery, bios. This is the file you edit.
- `assets/` — images. New uploads from the editor go into `assets/uploads/`.
- The games live in their own repos (ziv-vw/cat-chess, ziv-vw/twentyfour) and are hosted at chess.bat-cat.net and 24.bat-cat.net. Each project's *Link to play* points there.
- `index.html`, `support.js`, `image-slot.js` — the page design. Leave these alone unless you're changing the layout.

## One-time setup (about 15 minutes)

1. **GitHub** — create a free account at github.com, then *New repository* → name it `batcat-site` → *Create*.
   On the empty repo page click *uploading an existing file*, drag in everything in this folder (including `.pages.yml`; on a Mac press Cmd+Shift+. to show hidden files), then *Commit changes*.
2. **Cloudflare Pages** — dash.cloudflare.com → *Workers & Pages* → *Create* → *Pages* → *Connect to Git* → pick `batcat-site`.
   Build settings: framework **None**, build command **empty**, output directory **/**. Deploy.
3. **Domain** — in the Pages project → *Custom domains* → add `bat-cat.net` (and `www.bat-cat.net`). DNS is filled in automatically.
4. **Editor** — go to app.pagescms.org, sign in with GitHub, open `batcat-site`. You'll see forms for Journal entries, Projects, Cat gallery and About us.
   To let zii and ziu post too, add them as collaborators on the GitHub repo (Settings → Collaborators).

## Editing on the site itself

Once the batcat API Worker is set up (see the separate batcat-api guide), click **edit** in the footer on bat-cat.net, sign in, and add entries, projects and cat photos right on the page. That's the easiest way, and it works on your phone.

## Day to day (editing through GitHub / Pages CMS)

- **New journal entry**: Pages CMS → Site content → Journal entries → *Add* → fill in → *Save*. It's live in about a minute.
  The *Project id* must match a project's id (e.g. `cardigan`, `catchess`, `p24`).
- **Knitting patterns & progress photos**: add them to the entry's *Photos* field; they show when the entry is opened.
- **New gallery photo**: Cat gallery → *Add* → upload photo, caption, who.
- **New project**: Projects → *Add*. To link a game, host it (e.g. its own Cloudflare Pages project) and put its address in *Link to play*.

Editing `content.json` directly on github.com (pencil icon) works too — just keep the commas and quotes intact.
