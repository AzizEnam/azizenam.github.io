# azizenam.github.io

Source code for my personal website, hosted on GitHub Pages.

Powered by [SvelteKit](https://kit.svelte.dev/) and
[Tailwind CSS](https://tailwindcss.com/). To develop, run:

```sh-session
$ npm install
$ npm run dev
```

## Where to edit things

- **Home page** — `src/routes/+page.svelte`
- **Projects** — one Markdown file per project in `src/projects/` (see
  `example-project.md` for the format); intro text in
  `src/routes/projects/+page.svelte`
- **Resume** — `src/routes/resume/+page.svelte` (PDF source: `resume-src.html`)
- **Photo, name, nav, social links** — `src/lib/components/Sidebar.svelte`
- **Images / PDFs** — put files in `static/assets/` and link them as
  `/assets/...`
