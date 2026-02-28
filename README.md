# ERNIS Website (Jekyll + GitHub Pages)

This repository is configured as a **GitHub Pages project site**.

- Expected deploy URL: `https://USERNAME.github.io/ernis-research/`
- Local dev URL: `http://127.0.0.1:4000/ernis-research/`

Before publishing, update `USERNAME` in `/Users/arenberg/Documents/GitHub/ernis-research/_config.yml`.

## Run locally

```bash
bundle install
bundle exec jekyll serve
```

## How to update the site

### 1) Add a news item

Edit `/Users/arenberg/Documents/GitHub/ernis-research/_data/news.yml` and add one entry at the top:

```yaml
- date: 2026-03-01
  title: New preprint posted
  summary: "We released a new preprint on trustworthy adaptation."
  link: "https://example.com/preprint"
```

Required fields: `date`, `title`, `summary`.

### 2) Add a team member

Edit `/Users/arenberg/Documents/GitHub/ernis-research/_data/team.yml` and add an entry:

```yaml
- name: New Member
  role: PhD Student
  affiliation: Example University
  bio: "Short bio here."
  interests:
    - Topic A
    - Topic B
  email: new.member@example.edu
  website: https://example.com/new-member
  photo: /assets/images/team/new-member.jpg
  classes:
    - PhD Students
  status: current
  start_year: 2026
  end_year:
```

Fields used by the site:

- `name`
- `role`
- `affiliation`
- `bio`
- `interests`
- `email` (optional)
- `website` (optional)
- `photo` (optional)
- `classes` (one or more of: `Team Members`, `PhD Students`, `Master Students`, `Previous Members`)
- `status` (`current` or `alumni`)
- `start_year`
- `end_year` (optional)

### 3) Add a blog post

Create a new Markdown file in `/Users/arenberg/Documents/GitHub/ernis-research/_posts/` named:

`YYYY-MM-DD-short-title.md`

Use this front matter:

```yaml
---
title: "Post title"
date: 2026-03-01
authors:
  - Your Name
tags:
  - tag-one
  - tag-two
summary: "1-2 sentence summary."
featured_image: /assets/images/blog/example.jpg
prompt_title: "Prompt used for this post"
prompt: |-
  Write a short blog post about ...
---
```

Then add your post content below the front matter.

`prompt` and `prompt_title` are optional. If provided, they are shown in a dedicated Prompt section on the post page.

For multiple prompts in one post, use:

```yaml
prompts:
  - title: "Initial prompt"
    text: |-
      First prompt text...
  - title: "Refinement prompt"
    text: |-
      Second prompt text...
```

### Blog Markdown support

Blog post content uses core GitHub Flavored Markdown behavior through Jekyll `kramdown` + `GFM` input, with scoped GitHub-like styling on post pages.

Supported core syntax includes:

- Fenced code blocks with language highlighting
- Tables
- Task lists (`- [ ]` / `- [x]`)
- Strikethrough (`~~text~~`)
- Autolink-style URLs and standard Markdown links
- Blockquotes, nested lists, and inline code

Non-goals:

- No unsupported GitHub Pages plugins are added
- No guarantee for non-core GitHub-only extensions beyond standard GFM/kramdown support

### 4) Add a team photo with caption

1. Put your image in `/Users/arenberg/Documents/GitHub/ernis-research/assets/images/team/`.
2. Edit `/Users/arenberg/Documents/GitHub/ernis-research/_data/photos.yml`.
3. Add one entry:

```yaml
- image: /assets/images/team/your-photo.jpg
  caption: Your caption here
```

The page is available at `/photos/`.

## Notes

- Navigation and page links use Jekyll `relative_url`, so they work with `baseurl`.
- This setup stays GitHub Pages compatible by using the `github-pages` gem and supported plugins.

## Design references used

- [Stanford NLP](https://www-nlp.stanford.edu/)
- [SALT Lab (Stanford)](https://saltlab.stanford.edu/)
- [Allen Institute for AI](https://allenai.org/)
