# AC Fashion — Render deploy package

A single static page (`index.html`, all images inlined). No build step, no dependencies.

## Contents
- `index.html` — the whole AC Fashion pearl jewelry store site
- `render.yaml` — Render blueprint: one static site named `acfashionstudio`, publish path `.`

## How it goes live on Render
Render hosts static sites from a Git repository, so the steps are:

1. Put this folder in a GitHub (or GitLab) repository.
2. In Render: **New → Static Site** (or **New → Blueprint** and pick this repo, which reads `render.yaml` automatically).
3. Name: `acfashionstudio` · Build command: *(empty)* · Publish directory: `.`
4. Create. Render assigns the address `acfashionstudio.onrender.com` (if the name is taken, Render adds a suffix).

## Updating the store later
Replace `index.html` with a fresh export of the site, commit, and Render redeploys automatically.
Note: edits made to the site inside Muse do NOT flow to Render on their own — each update is a new export + commit.
