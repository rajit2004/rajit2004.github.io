# rajit2004.github.io

My personal portfolio and homepage, hosted on GitHub Pages at [rajit2004.github.io](https://rajit2004.github.io/).

## About

A single-page portfolio for **Ranesh Rajit**, a B.Tech CS student focused on Java, DSA, and open source. The site is built as one self-contained HTML file with no frameworks and no build step, so it loads fast and is easy to keep up to date.

## Features

- **Hero** with typewriter roles, staggered entrance animation, and orbit rings
- **Real-time stats** pulled live from the GitHub API and LeetCode, with a 30-minute cache and offline fallbacks
- **Projects grid** with 3D tilt, cursor-follow glow, and hover states
- **Interactive skills** that pop open a proficiency popover with level bars when clicked
- **Open source section** showing live merged-PR counts per repo
- **Contact cards** and an availability status pill
- **Polish**: preloader, scrolling tech marquee, scroll progress bar, scrollspy nav, magnetic buttons, custom animated cursor, aurora background, film grain, and back-to-top button
- Respects `prefers-reduced-motion`

## Getting Started

There is nothing to install or build. Open the site directly:

```bash
# Serve locally (any static server works)
python -m http.server 8080 --directory docs
```

Then visit `http://localhost:8080`.

## Project Structure

```
.
├── .gitignore
├── README.md
└── docs/
    └── index.html   # the entire site (HTML, CSS, and JS)
```

## Deployment

GitHub Pages is configured to publish from the `/docs` folder on `main`. Pushing to `main` triggers the automatic Pages deployment, so there is no build step to run.

## Live Stats

The stats bar (problems solved, PRs merged, stars, followers, repos) updates itself from:

- [LeetCode GraphQL API](https://leetcode.com/rajit2004/) via a community proxy
- GitHub REST API (`api.github.com`)

Values are cached in `localStorage` for 30 minutes so the page does not hammer the APIs on every visit, and it falls back to sensible defaults if a request fails.

## License

This is a personal portfolio. You are welcome to look around, but please do not copy the design wholesale for your own portfolio.
