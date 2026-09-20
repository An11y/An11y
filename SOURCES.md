# Sources — APIs & widgets for a killer GitHub profile

Free image/SVG endpoints you can drop into a profile README.  
No SDK. Copy URL → paste in Markdown.

---

## Core (used in this README)

| What | Repo / site | Endpoint pattern |
|:-----|:------------|:-----------------|
| **Header / footer waves** | [capsule-render](https://github.com/kyechan99/capsule-render) | `https://capsule-render.vercel.app/api?type=waving&color=...&text=...` |
| **Typing animation** | [readme-typing-svg](https://github.com/DenverCoder1/readme-typing-svg) | `https://readme-typing-svg.demolab.com?font=...&lines=A;B` |
| **Stats card** | [github-readme-stats](https://github.com/anuraghazra/github-readme-stats) | `https://github-readme-stats.vercel.app/api?username=USER` |
| **Repo pin cards** | same | `.../api/pin/?username=USER&repo=REPO` |
| **Top languages** | same | `.../api/top-langs/?username=USER&layout=compact` |
| **Commit streak** | [github-readme-streak-stats](https://github.com/DenverCoder1/github-readme-streak-stats) | `https://streak-stats.demolab.com?user=USER` |
| **Trophies** | [github-profile-trophy](https://github.com/ryo-ma/github-profile-trophy) | `https://github-profile-trophy.vercel.app/?username=USER` |
| **Activity graph** | [github-readme-activity-graph](https://github.com/Ashutosh00710/github-readme-activity-graph) | `https://github-readme-activity-graph.vercel.app/graph?username=USER` |
| **Contribution snake (hosted)** | [MZR Icons](https://icons.mzrdev.com/) | `https://icon.mzrdev.com/snk?username=USER&palette=github-dark` |
| **Tech icons grid** | [skillicons](https://skillicons.dev) | `https://skillicons.dev/icons?i=ts,react,docker` |
| **Classic badges** | [shields.io](https://shields.io) | `https://img.shields.io/badge/...` |
| **Profile view counter** | [ghpvc](https://github.com/antonkomarev/github-profile-views-counter) | `https://komarev.com/ghpvc/?username=USER` |
| **Random quote** | [github-readme-quotes](https://github.com/PiyushSuthar/github-readme-quotes) | `https://quote-github-readme.vercel.app/api?type=horizontal&theme=tokyonight` |

---

## Extra APIs worth adding

### All-in-one widget hubs

| Project | Why use it |
|:--------|:-----------|
| **[MZR Icons](https://icons.mzrdev.com/)** · [repo](https://github.com/MZRCode/mzr-icons) | One host for trophies, streaks, typing, snake, 400+ icons: `/trophy` `/stats` `/snk` `/typing` `/badge` `/icons/:name` |
| **[GitWidgets](https://github.com/LeGi0N09/GitWidgets)** | Skills matrix, profile banner, profile tag, skill tag, commit streak — themeable widgets |

### Self-hosted / Actions (more control)

| Project | Why use it |
|:--------|:-----------|
| **[Platane/snk](https://github.com/Platane/snk)** | Generate snake SVG/GIF via GitHub Action every day (best quality, dark-mode `<picture>`) |
| **Self-host github-readme-stats** | Avoid public Vercel rate limits; deploy your own fork |

### Generators (UI → copy Markdown)

| Tool | Link |
|:-----|:-----|
| GitHub Profile README Generator | https://rahuldkjain.github.io/gh-profile-readme-generator/ |
| Profile Me | https://profileme.dev/ |
| Arturito README | https://arturito.vercel.app/ |

---

## Quick copy — An11y

```md
<!-- stats -->
![](https://github-readme-stats.vercel.app/api?username=An11y&theme=tokyonight&hide_border=true&bg_color=0B0E14)

<!-- streak -->
![](https://streak-stats.demolab.com?user=An11y&theme=tokyonight&hide_border=true&background=0B0E14)

<!-- languages -->
![](https://github-readme-stats.vercel.app/api/top-langs/?username=An11y&layout=compact&theme=tokyonight&hide_border=true&bg_color=0B0E14)

<!-- trophies -->
![](https://github-profile-trophy.vercel.app/?username=An11y&theme=tokyonight&no-frame=true&no-bg=true&column=7)

<!-- activity -->
![](https://github-readme-activity-graph.vercel.app/graph?username=An11y&bg_color=0B0E14&color=38BDF8&line=818CF8&area=true&hide_border=true)

<!-- snake (MZR) -->
![](https://icon.mzrdev.com/snk?username=An11y&palette=github-dark)

<!-- skills -->
![](https://skillicons.dev/icons?i=ts,js,react,nextjs,nodejs,python,docker,linux,git)

<!-- typing -->
![](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=26&color=38BDF8&center=true&lines=Ship+fast;Build+clean)

<!-- views -->
![](https://komarev.com/ghpvc/?username=An11y&style=for-the-badge&color=6366f1)
```

---

## Tips so it stays “pizdato”, not spammy

1. **One visual language** — same bg (`0B0E14`), accents (`38BDF8` / `6366F1`), one theme family (`tokyonight`).
2. **Don’t stack every widget** — header + typing + 3 pins + stats/streak + graph/snake is enough.
3. **`count_private=true`** on stats only works if the stats service has a PAT (self-host) or you accept public-only numbers on the public API.
4. **Rate limits** — public Vercel demos occasionally 429; MZR / self-host / Platane Action are more reliable for snake.
5. **Dark mode** — for Platane snake use `<picture>` with light/dark `srcset`.

---

## Official GitHub docs

- [About your profile README](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)
- Special repo name must be **exactly** `USERNAME/USERNAME` (here: `An11y/An11y`)
- README must be on the **default branch** (`main`)
