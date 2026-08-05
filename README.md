# rajit2004.github.io

My personal portfolio and homepage, hosted on GitHub Pages at [rajit2004.github.io](https://rajit2004.github.io/).

## About

A single-page portfolio for **Ranesh Rajit**, a B.Tech CS student focused on Java, DSA, and open source. The site is built as one self-contained HTML file with no frameworks and no build step, so it loads fast and is easy to keep up to date.

## Features

- **Hero** with a live `LOGS:LIVE` status badge, typewriter roles, staggered entrance animation, orbit rings, and at-a-glance facts. On the right, a single **system-console panel** merges a DSA progress gauge (problems/yr ring), a live ticking IST clock, a compact "currently" feed (building/learning/grinding/open-to that auto-rotates, with click-to-focus), a real GitHub contribution heatmap (12 weeks, cached with a fallback pattern), and a rotating mission-log line. The name auto-scales to fill the hero width on desktop, measured with the canvas API (no layout reflow)
- **System-console accents** throughout: `$` shell-command section eyebrows (`$ ls ./works`, `$ git log --merged`), `//` section numbers, and PID-styled skill groups
- **Click effects**: amber ink-ripples on chips, cards, and buttons; the system-monitor panel emits an "ACK" pulse ring; the Currently cards are clickable to focus that card; heatmap cells scale up with a date/count tooltip on hover
- **Real-time stats** pulled live from the GitHub API and LeetCode, with a 30-minute cache and offline fallbacks
- **Projects grid** with 3D tilt, cursor-follow glow, hover states, and **live GitHub star counts** per repo
- **Interactive skills** that pop open a proficiency popover with level bars when clicked
- **Open source section** showing live merged-PR counts per repo
- **Achievements section** highlighting recognition, reach, and open source programs
- **Contact section** with an availability status pill and a prominent "Open to work" CTA
- **Polish**: preloader, scrolling tech marquee, scroll progress bar, scrollspy nav, magnetic buttons, custom animated cursor, aurora background, film grain, back-to-top button, and a responsive hamburger menu on mobile
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

The stats bar (problems solved, PRs merged, stars, followers, repos) and the star counts on project cards update themselves from:

- [LeetCode GraphQL API](https://leetcode.com/rajit2004/) via a community proxy
- GitHub REST API (`api.github.com`)

Values are cached in `localStorage` for 30 minutes so the page does not hammer the APIs on every visit, and it falls back to sensible defaults if a request fails.

## License

This is a personal portfolio. You are welcome to look around, but please do not copy the design wholesale for your own portfolio.
