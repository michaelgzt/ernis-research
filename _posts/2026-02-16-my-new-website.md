---
title: My new personal and team website is online
date: 2026-02-16
authors:
  - Guangzhi Tang
tags:
  - views
summary: Why do I decide to create a new personal website? An end result of existential crisis with vibe coding and a new platform to post views from my entire team.
prompts:
  - title: "Prompt for polishing this blog using ChatGPT 5.2 Thinking"
    text: |-
      Review the following text I wrote for my blog. Fix grammar problems and make it easy to read for non-technical audiences. Do not change any view or format in the text. Explain your changes one by one.
  - title: "Initial prompt for building my personal website using ChatGPT 5.3 Codex"
    text: |-
      Goal: Create a GitHub Pages personal + research team website that is easy to maintain by editing Markdown/YAML files (no code changes needed for most updates). Use Jekyll and a GitHub-Pages-compatible setup.
      Repo type: (choose one and implement accordingly)
      If this is my main site: repository name USERNAME.github.io and it should deploy at https://USERNAME.github.io/.
      Otherwise: deploy as a project site at https://USERNAME.github.io/REPO/ and ensure links work with baseurl.
      Site requirements
      Pages / navigation
      Home (/): short intro (photo optional placeholder), research summary, and a News section (reverse chronological).
      Team (/team/): current members + alumni/previous students.
      Blog (/blog/): blog index and individual posts by me and my students.
      Top nav + footer with contact links.
      Content model (make it easy to add/edit content)
      Store news items in a simple file (prefer _data/news.yml or a news collection) so I can add one entry at a time.
      Store team members in _data/team.yml (or a people collection). Include fields: name, role, affiliation, bio, interests, email (optional), website (optional), photo (optional), status (current or alumni), start_year, end_year (optional).
      Store blog posts in _posts/ as Markdown with front matter: title, date, authors, tags, summary, and optional featured_image.
      Add a lightweight “How to update the site” section in README.md explaining exactly how to add a news item, add a team member, and add a blog post.
      Design / UX
      Clean academic style, responsive, accessible.
      Consistent typography, simple layout, no heavy JS frameworks.
      Blog should support tags (basic tag pages or tag filtering is fine).
      Add an RSS feed for posts.
      GitHub Pages compatibility
      Use a GitHub Pages–supported Jekyll configuration (avoid unsupported plugins).
      Include a Gemfile using the github-pages gem for local parity.
      Provide commands to run locally (bundle install + serve).
      Deliverables
      Full working site structure: layouts, includes, CSS, sample content.
      _config.yml correctly configured for user site OR project site (url/baseurl handled).
      Add at least:
      3 sample news items
      6 sample team entries (mix of current + alumni)
      2 sample blog posts with different authors
      Add an AGENTS.md (or equivalent) telling Codex to keep changes GitHub Pages compatible and prefer editing content files over templates when possible.
      Acceptance criteria (verify)
      bundle exec jekyll serve runs locally with no errors.
      Home, Team, Blog pages render and show sample content.
      Links work in both local dev and the expected GitHub Pages URL.
      Please implement this end-to-end in the repo, creating all necessary files and directories.
---
I recently started using coding agents, like Claude Code, more extensively to help me understand students' code and implement new ideas. I have to admit that it works great, especially for a person like me who doesn't have much time for coding due to the nature of my job at the university. However, it has also started to give me an existential crisis, making me question whether I'm still needed in the loop. After two weeks of vibe coding, I want to put some of my random thoughts here:

1. I have been using Claude and ChatGPT conversations to help me code from the very start. But coding agents are the first time I have felt that this thing can fully replace me. I want to say that now we are truly at the edge of a new industrial revolution.

2. Good tests are the key for something like Claude Code to generate correct and useful code. I used it to refactor my students' old code for training neural networks. However, it can make mistakes sometimes and even pass tests it designed itself. This really eroded my trust in the generated code and made me spend time reading through the code to see whether the agent coded the most critical parts correctly.

3. What's my contribution in this loop? I have to admit I also use LLMs for ideas, since research most of the time is about building on top of old ideas, combining multiple ideas, and transferring ideas from one domain to another. With LLMs and coding agents, this process will be much faster than before. Many influential papers are just the result of a more dedicated PhD student who tried more combinations and experiments than others.

4. How will our computer science education change? With coding agents, now we need to train more drivers but fewer car engineers. Of course, currently the car is still like a prototype that you still need to repair sometimes. But very soon, the car will mature. Then we only need drivers who know where they want to go, and everyone can be a driver after several months of part-time learning.

And more thoughts to come. Hopefully soon, I will share my first research project fully done with LLM agents without help from any students or team members, which is currently in progress.

Back to the new personal website. The small project started just to try the new ChatGPT 5.3 Codex. I was a loyal user of Claude Code, but the tight token limit really annoyed me and made me decide to try something else. During the process, I figured the best demo project would be just making a new website.

I started with a prompt generated with the help of ChatGPT (I attached the prompt at the end). But this did not magically solve the problem in one go. I had to do multiple rounds of conversations with Codex to improve the style, move components, add new pages, and delete things I don't like. The end result is not perfect. I may still need to improve it for the rest of the year, but I like it.

The most important goal of this new website, which was not there in my previous website, is to show my team, my students, and my team's personal views. This reflects my transition from an individual researcher to someone who needs to lead people to do research and educate students on how to do research. It's not an easy time for this transition, as many things that were mostly unchanged in the last ten years are starting to change drastically now. I didn't have LLMs and coding agents during my PhD years. Nowadays, an undergraduate student can easily do things that I needed a steep learning curve to do during my PhD. And it is so easy to understand research progress with the help of LLMs that incremental research can become a one-day task.

Therefore, I expect the end goal of this website is for it to be a platform to help everyone on my team share their different views on the research they are working on, and on how this new industrial revolution will change things in the university and industry. I hope this works, and more to come.
