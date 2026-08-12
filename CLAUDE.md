# shreyas-viswanathan-portfolio

React + Vite personal portfolio site for Shreyas Viswanathan. Built on the React Portfolio Template (Bootstrap 5), heavily customized.

## Content model

All page copy lives in JSON under `public/data/`, not in JSX. Section components (`src/components/sections`, `src/components/articles`) render whatever these files describe:

- `public/data/sections.json`, `public/data/categories.json`, `public/data/profile.json`, `public/data/settings.json`, `public/data/strings.json`
- `public/data/sections/*.json` — one file per page section (`cover`, `experience`, `education`, `skills`, `achievements`, `portfolio`, `updates`, `contact`)

Every user-facing string sits under a `"locales"` object keyed by language: `en` (source of truth), `fr`, `hi`, `ta` (some UI-chrome-only strings also carry `es`/`ko`). **When editing content, update all of en/fr/hi/ta together** — leaving one locale stale is the most common mistake in this repo.

## Commands

- `npm run dev` — local dev server
- `npm run build` — production build to `dist/`
- `npm run lint` — ESLint

## Notes

- `dist/` is a build artifact (gitignored) — never hand-edit it; edit `public/data/` and rebuild.
- No test suite in this repo.
