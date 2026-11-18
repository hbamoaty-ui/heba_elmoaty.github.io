# How to publish an article

Your site now uses Jekyll, which GitHub Pages runs for you automatically. Every article is one Markdown file. Add the file, and the site rebuilds by itself in about a minute.

## Put the site online (one time) with GitHub Desktop

The GitHub website can't upload folders reliably, so use the free GitHub Desktop app.

1. Delete the old repository: on GitHub open it → **Settings** → scroll to the bottom → **Delete this repository**.
2. Install GitHub Desktop from desktop.github.com and sign in with your GitHub account.
3. Unzip `website-update.zip`. You get a folder called `website-update`.
4. In GitHub Desktop: **File → Add Local Repository…** → choose the `website-update` folder → click **create a repository** → **Create Repository**.
5. Click **Publish repository**. Set the name to exactly `heba_elmoaty.github.io`, **untick** "Keep this code private", then click **Publish Repository**.
6. Wait 1–2 minutes and open https://hbamoaty-ui.github.io/heba_elmoaty.github.io/

To change the site later: edit the files in the `website-update` folder, then in GitHub Desktop write a short summary and click **Commit to main** → **Push origin**.

## Publish a new article

1. In your repository (github.com/hbamoaty-ui/heba_elmoaty.github.io), open the `_drafts` folder and open one of the templates (English or Arabic). Copy its contents.
2. Go back to the main page of the repository and click **Add file → Create new file**.
3. In the name box, type `_posts/` then the file name, using this pattern: `_posts/YYYY-MM-DD-short-english-name.md`
   - Example: `_posts/2026-11-20-words-that-help.md`
   - Typing `_posts/` creates the folder the first time.
   - The date is the publish date. The name becomes the link: `.../articles/words-that-help/`
   - Use English letters and dashes in the file name, even for Arabic articles.
4. Paste the template, then replace the title, description and text with your article.
5. Click **Commit changes**. The article appears on the homepage and on the Articles page within a minute or two.

## The settings at the top of each article

```yaml
---
title: "Your title"
description: "Shown on the article card and in LinkedIn previews."
lang: en          # en = English, ar = Arabic (the page switches to right-to-left)
cover: /assets/articles/words-that-help/cover.png   # optional
cover_alt: "What the image shows"
tags: [UX writing, Content design]
---
```

## Add images

1. Go to `assets/articles`, click **Add file → Upload files**, and upload your images into a folder named after the article, such as `assets/articles/words-that-help/`.
2. Use the cover image in the settings: `cover: /assets/articles/words-that-help/cover.png`
3. Insert an image inside the text:

```markdown
![What the image shows]({{ site.baseurl }}/assets/articles/words-that-help/screen-1.png)
*Optional caption on the next line.*
```

Keep images under about 500 KB so pages load quickly.

## Edit or remove an article

- **Edit:** open the file in `_posts`, click the pencil icon, change it, commit.
- **Unpublish:** move it back to `_drafts` (rename it to `_drafts/name.md`), or delete it.
- **Schedule:** a file dated in the future won't appear until that date, and only after your next commit on or after that date.

## What changed in the site

- New look: dark theme by default (light theme on the moon button), floating pill menu that also works on phones, a hero where the highlighted word changes like a live edit, app screens in phone frames, four feature cards that open the matching use case, and a big footer card with your contact details, rotating use-case quotes, and your name as a wordmark.

- Styles moved to `assets/css/main.css` so the homepage and article pages share one design.
- Header, footer and page meta live in `_includes/` and appear on every page.
- The Writing section on the homepage now shows your 3 newest articles from this site, then your Medium articles under **Earlier, on Medium**.
- New **Articles** page at `/articles/` lists all articles with an English/Arabic filter.
- Each article page has reading time, cover image, tags, share links (LinkedIn, X, copy link), an author box, and links to the newer and older articles.
- RSS feed at `/feed.xml` for anyone who wants to subscribe.
