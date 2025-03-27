# README

**Note**: This file is **not** intended to appear on the live website. It’s for internal documentation, explaining how to work with this Jekyll site, how to add new pages, announcements, images, and more.

---

## Table of Contents

1. [What This Website Is](#what-this-website-is)
2. [How It Works (Jekyll, GitHub Pages, Just the Docs)](#how-it-works-jekyll-github-pages-just-the-docs)
3. [Adding a New Page](#adding-a-new-page)
4. [Adding Announcements](#adding-announcements)
5. [Child Pages & Navigation](#child-pages--navigation)
6. [Images & Assets](#images--assets)
7. [Formatting Content (Markdown & Just the Docs)](#formatting-content-markdown--just-the-docs)
8. [Using ChatGPT for Assistance](#using-chatgpt-for-assistance)
9. [Directory Structure Overview](#directory-structure-overview)

---

## What This Website Is

This repository hosts a **Jekyll-based website** published via **GitHub Pages**.  
- We use the [**Just the Docs**](https://just-the-docs.github.io/just-the-docs/) Jekyll theme to style our documentation and provide a sidebar/navigation structure.

The primary purpose of the site is to share information about the UoM Robotics Society’s 2025 Hack-A-Bot event, including:
- A home page (introduction and quick links)
- Detailed tasks
- Schedules
- Announcements
- General hackathon info (rules, guidelines, volunteer info, etc.)

---

## How It Works (Jekyll, GitHub Pages, Just the Docs)

1. **Jekyll**  
   Jekyll is a static site generator that turns `.md` and `.html` files into a complete static website. When changes are pushed to the `main` (or relevant) branch, GitHub Pages automatically rebuilds the site.

2. **GitHub Pages**  
   GitHub Pages hosts your Jekyll site for free. Whenever you commit to the default branch (often `main`), GitHub will rebuild and update the live site at the specified URL (e.g., `https://aj-floater.github.io-1/`).

3. **Just the Docs**  
   This is the theme providing the layout, navigation, and styling. It offers:
   - Automatic table of contents
   - Search functionality
   - Easy front matter control for page ordering and sidebar headings

---

## Adding a New Page

1. **Create a Markdown File**  
   In the `docs/` folder (or a subfolder within it), create a new `.md` file. For instance, `docs/my-new-page.md`.

2. **Front Matter**  
   At the top of your `.md`, include something like:
   ```yaml
   ---
   title: My New Page
   layout: default
   nav_order: 10
   ---
   ```
   - `title` is what appears in the page header and the sidebar.
   - `layout: default` uses the Just the Docs base layout.
   - `nav_order` controls the page’s order in the sidebar (lower = higher on the list, so choose carefully).

3. **Write Your Content**  
   Use Markdown to format headings, paragraphs, images, code blocks, etc.  
   For example:
   ```markdown
   # My New Page

   Welcome to this new page with important hackathon info.
   ```

4. **Commit & Push**  
   Once you push changes to the repo, GitHub Pages will rebuild. Your new page will appear in the sidebar if you have **just-the-docs** style navigation set up in `_config.yml`.

---

## Adding Announcements

We have a custom [announcements collection] in `docs/_announcements`:
1. **Create a new file** in `docs/_announcements` (e.g., `2025-04-01-robotics-demo.md`).
2. **Front Matter** might look like:
   ```yaml
   ---
   title: "Robotics Demo"
   author: "Izzy"
   date: 2025-04-01 15:00:00
   ---
   ```
   - `title`: short announcement title
   - `author`: who posted it
   - `date`: date and time
3. **Add your content** below the front matter. Markdown formatting is allowed:
   ```markdown
   The Makerspace will host a special robotics demo at 3 PM.
   ```
4. **Save/Commit/Push**. The file will automatically appear under [Announcements](../announcements.md) (the main announcements page) once the site rebuilds.

---

## Child Pages & Navigation

- **Hierarchy**: You can organize pages in subfolders (like `docs/tasks/`) and link them in the main `tasks.md` or use front matter to nest them under a parent.  
- **nav_order** & **parent**: In the `_config.yml` or within each page, you can define the hierarchy. See [Just the Docs navigation docs](https://just-the-docs.github.io/just-the-docs/docs/navigation-structure/) for details.

Example front matter for a child page:
```yaml
---
title: "Task 1"
parent: "Tasks"  # The exact title of the parent page
nav_order: 1
---
```

---

## Images & Assets

1. Place images in `docs/assets/images` or a subfolder (like `docs/assets/images/organisers`).
2. Reference them in Markdown with a relative path:
   ```markdown
   ![Team Photo](/docs/assets/images/organisers/teamphoto.png)
   ```
   or using Jekyll’s relative_url filter:
   ```markdown
   ![Team Photo]({{ '/docs/assets/images/organisers/teamphoto.png' | relative_url }})
   ```
3. **Sizing or alignment**: Use standard Markdown image syntax or inline HTML for more control:
   ```markdown
   <img src="{{ '/docs/assets/images/organisers/teamphoto.png' | relative_url }}" width="300" alt="Team Photo" />
   ```

---

## Formatting Content (Markdown & Just the Docs)

**Headings**  
Use `# H1`, `## H2`, `### H3`, etc.

**Code Blocks**  
Use triple backticks (```) for fenced code blocks. E.g.,
````markdown
```bash
echo "Hello World"
```
````
You can specify the language (like `bash`, `python`, `javascript`) for syntax highlighting.

**Tables**  
Use standard Markdown table syntax:
```markdown
| Column A | Column B |
|----------|----------|
| Row 1    | Row 1    |
| Row 2    | Row 2    |
```

**Lists**  
- Use `-` or `*` for unordered lists.
- Use `1., 2., 3.` for ordered lists.

**Just the Docs**  
- Provides built-in [search](https://just-the-docs.github.io/just-the-docs/docs/search/).
- Allows [custom color schemes](https://just-the-docs.github.io/just-the-docs/docs/color-settings/).
- Manage site settings in `_config.yml`.

---

## Using ChatGPT for Assistance

When you need help **formatting content in Markdown** or generating boilerplate text:
1. Go to ChatGPT (or your AI tool of choice).
2. Provide the rough text and ask for a “nicely formatted Markdown” version.  
3. Copy the result into your `.md` file.

**Tip**: You can also ask ChatGPT to generate code blocks, tables, or entire page structures for you. Just remember to review for accuracy before committing!

---

## Directory Structure Overview

Here’s a simplified look at the important parts:

```
aj-floater.github.io-1/
├── .github/                # GitHub-related configs (e.g., workflows)
├── .gitignore
├── .vscode/
├── Gemfile, Gemfile.lock   # Ruby dependencies for Jekyll
├── LICENSE
├── README.md               # (THIS FILE) Internal documentation
├── _config.yml             # Main Jekyll configuration & Just the Docs settings
├── _site/                  # Generated site (do not edit manually)
└── docs/                   # Actual site content
    ├── _announcements/     # Markdown files for each announcement
    ├── _sass/              # SCSS files for custom styling
    ├── announcements.md    # The main Announcements index page
    ├── assets/             # Images, CSS, and other static files
    ├── index.md            # Homepage
    ├── schedule.md         # Schedule page
    └── tasks/             # Folder for task pages
        ├── Task 1.md
        ├── Task 2.md
        └── Task 3.md
```

- **docs/** is where you’ll spend most of your time adding or updating pages.  
- **_site/** is auto-generated on build. Don’t manually change anything in `_site/`.  
- **Gemfile** / **Gemfile.lock** manage Jekyll’s plugins and theme dependencies.  

---

**That’s it!** If you have any questions or run into issues, check the [Jekyll documentation](https://jekyllrb.com/) or ping Archie. The site should remain straightforward to update thanks to Markdown, Just the Docs, and GitHub Pages. Enjoy! 