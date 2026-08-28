# Samith Va

Personal technical blog built with [Hugo](https://gohugo.io/) and the
[PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. The site is
published at <https://samithva.github.io/>.

## Local development

Requirements:

- Hugo Extended 0.164.0 or newer
- Git with submodule support

Clone the repository and initialize the PaperMod theme:

```bash
git clone --recurse-submodules https://github.com/SamithVa/samithva.github.io.git
cd samithva.github.io
hugo server -D
```

Open <http://localhost:1313/>. Build the production site with:

```bash
hugo --gc --minify
```

Generated output is written to `public/` and is not committed.

## Content

Posts live in `content/posts/` as leaf bundles. Keep each post's Markdown and
images in the same directory:

```text
content/posts/topic/post-name/
|-- index.md
|-- cover.png
`-- figure.png
```

Create a draft with:

```bash
hugo new content posts/topic/post-name/index.md
```

Use standard fenced code blocks for source examples. The site also supports the
`notice` and `image-grid` shortcodes:

```markdown
{{</* notice note title="Optional title" */>}}
Important content.
{{</* /notice */>}}

{{</* image-grid */>}}
![First image](first.png)
![Second image](second.png)
{{</* /image-grid */>}}
```

Mermaid diagrams use a normal `mermaid` fenced code block.

## Theme updates

PaperMod is tracked from `SamithVa/hugo-PaperMod` as a Git submodule:

```bash
git submodule update --remote --merge themes/PaperMod
```

Review and commit the resulting submodule pointer after testing the site.

## Deployment

Pushes to `main` run `.github/workflows/hugo.yml`. The workflow builds Hugo,
uploads the generated site, and deploys it to GitHub Pages. In the repository's
Pages settings, set the publishing source to **GitHub Actions**.
