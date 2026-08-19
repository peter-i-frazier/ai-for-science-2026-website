# ai-for-science-2026-website

Website for the Fall 2026 AI for Science course (ORIE 7190) at Cornell.

Live at: https://peter-i-frazier.github.io/ai-for-science-2026-website/

## Editing

Everything is markdown, rendered by GitHub Pages with the Cayman theme. Edit and push; there is no build step to run locally.

- `index.md` --- the course page
- `syllabus.md` --- the full syllabus, adapted from Fall 2023
- `topics.md` --- the running list of topics and resources
- `_config.yml` --- site title and theme

## One-time setup

Enable Pages: repo Settings -> Pages -> Source "Deploy from a branch" -> `main` / `/ (root)`.

## To stop and start the Jekyll server

pkill -f "jekyll serve"

cd ~/git/ai-for-science-2026-website
PATH="/opt/homebrew/opt/ruby/bin:$PATH" bundle exec jekyll serve --livereload

This is needed when we change the _config.yml but not on updates the page content.pkill -f "jekyll serve"

## To-do items

- Add these items to the syllabus page:
	- Course schedule
	- Office hours
	- Course slack
	- Gradescope (gradescope entry code)
