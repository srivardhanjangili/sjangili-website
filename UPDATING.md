# Updating your website

Everything below can be done in the browser on GitHub: open the file, click the pencil icon, edit, and click **Commit changes**. The live site updates about two minutes after each commit to `main`.

## Papers — `data/papers.yaml`

**Add a paper:** copy an existing entry (from `- title:` down to `job_market_paper:`) and edit it. To attach a PDF, upload it to `static/files/` (Add file → Upload files) and set `pdf: "files/your-file.pdf"`.

**Mark a paper published:** change `status` to `published`, fill in `venue` (the journal) and `year`, and put the DOI link in `link`. It moves from "Working papers" to "Publications" automatically.

Status options: `published`, `accepted`, `revise and resubmit`, `under review`, `working paper`, `work in progress`.

**Job market paper:** set `job_market_paper: true` on one paper and add an `abstract`. It gets a highlighted card at the top of Research.

**Abstracts:** fill in `abstract:` on any paper and it appears as a collapsible "Abstract" link.

## Teaching — `data/teaching.yaml`

Each entry has `course`, `role`, `institution`, and `term`. List several terms in one line, e.g. `"Fall 2025, Spring 2026"`.

## Presentations — `data/talks.yaml`

Each entry has `title`, `venue`, and `date`. Newest first.

## Awards — `data/awards.yaml`

Each entry has `name` and `year`.

## Bio — `content/_index.md`

Edit the paragraphs below the `---` lines. Leave a blank line between paragraphs.

The Research and Teaching pages are built from the data files above. Their titles and one-line descriptions are in `content/research/_index.md` and `content/teaching/_index.md`; any text you write below the `---` lines there appears at the top of that page.

## Title, email, links — `hugo.yaml`

Under `params:` you can change `role`, `interests`, `email`, and the `social` links.

## CV and photo

- **CV:** upload the new PDF to `static/files/` named exactly `cv.pdf` (it replaces the old one).
- **Photo:** upload a new image to `assets/images/` named exactly `photo.jpg`. It is cropped and resized automatically.

## Footer credit and invisible marker — `hugo.yaml`

`params.mysite.credit` shows a small "Created using GaryKing.org/mysite" line in the footer (currently `false`).
`params.mysite.discovery` adds a hidden generator tag and search-engine structured data (currently `true`). Set either to `false` or `true` to change.

## Changing the look

The colors and fonts live in `assets/css/style.css` (the `:root` block at the top). To change the look of the site, ask your assistant to run the design quest at https://gking.harvard.edu/mysite/files/QUEST_DESIGN.md and show you three previews.

## Previewing locally (optional)

Install [Hugo extended](https://gohugo.io/installation/), then run `hugo server` in this folder and open the address it prints.
