<div align="center">

<img src="https://i.imgur.com/GZHodUG.png" width="90px" alt="Streak Stats Logo"/>

# 🔥 GitHub Readme Streak Stats

**Track. Display. Inspire.**
Showcase your GitHub contribution streak on your profile — beautifully and effortlessly.

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-streak--stats.demolab.com-0d1117?style=for-the-badge&labelColor=238636)](https://streak-stats.demolab.com)
[![GitHub Stars](https://img.shields.io/github/stars/shahrozraza205-source/github-readme-streak-stats?style=for-the-badge&logo=github&color=0d1117&labelColor=238636)](https://github.com/shahrozraza205-source/github-readme-streak-stats/stargazers)
[![License MIT](https://img.shields.io/badge/License-MIT-0d1117?style=for-the-badge&labelColor=238636)](LICENSE)
[![Discord](https://img.shields.io/discord/819650821314052106?color=0d1117&logo=discord&logoColor=white&style=for-the-badge&label=Discord&labelColor=5865F2)](https://discord.gg/fPrdqh3Zfu)

---

[![GitHub Streak](https://streak-stats.demolab.com/?user=shahrozraza205-source&theme=dark&hide_border=true&ring=238636&fire=238636&currStreakLabel=238636)](https://github.com/shahrozraza205-source)

*Live streak card — powered by this very project.*

</div>

---

## 📋 Table of Contents

- [What Is This?](#-what-is-this)
- [Quick Setup](#-quick-setup)
- [Live Preview](#-live-preview)
- [Options & Parameters](#-options--parameters)
- [Themes](#-themes)
- [Date Formats](#-date-formats)
- [Locales](#-locales)
- [How Stats Are Calculated](#-how-stats-are-calculated)
- [Self-Hosting](#-self-hosting)
- [Contributing](#-contributing)
- [Support](#-support)

---

## 💡 What Is This?

**GitHub Readme Streak Stats** is an open-source tool that generates a dynamic stats card showing:

- 🟢 **Total Contributions** — Every commit, PR, and issue you've ever made
- 🔥 **Current Streak** — How many consecutive days you've contributed
- 🏆 **Longest Streak** — Your all-time best contribution streak

The card is generated as an SVG image that renders perfectly inside any GitHub profile README. It is lightweight, fast, and fully customizable — from colors and themes to date formats and locales.

---

## ⚡ Quick Setup

Getting started takes under a minute:

**Step 1** — Open your GitHub profile `README.md` and paste this:

```md
[![GitHub Streak](https://streak-stats.demolab.com/?user=shahrozraza205-source)](https://github.com/shahrozraza205-source)
```

**Step 2** — Your live streak card will appear automatically. No API key needed!

**Step 3** — Customize it using the parameters below, or use the [Demo Site](https://streak-stats.demolab.com) to preview changes in real time.

> 💡 **Pro Tip:** For maximum reliability and uptime, consider [self-hosting](#-self-hosting) your own instance — it only takes 2 minutes.

---

## 🎨 Live Preview

Try the interactive customizer — see your card update in real time before adding it to your profile:

🔗 **[streak-stats.demolab.com](https://streak-stats.demolab.com)**

[![Demo Site](https://user-images.githubusercontent.com/20955511/114579753-dbac8780-9c86-11eb-97dd-207039f67d20.gif)](http://streak-stats.demolab.com/demo/)

---

## ⚙️ Options & Parameters

The `user` parameter is **required**. Everything else is optional.

> If `theme` is set, any additional color options will **override** that theme's defaults.

| Parameter | Description | Default | Example Values |
|:---------:|:-----------:|:-------:|:--------------:|
| `user` | GitHub username | — | `shahrozraza205-source` |
| `theme` | Preset theme | `default` | `dark`, `radical`, [all themes ➜](./docs/themes.md) |
| `hide_border` | Transparent border | `false` | `true` / `false` |
| `border_radius` | Edge roundness | `4.5` | `0` (sharp) → `248` (ellipse) |
| `background` | Background color | — | Hex (no `#`), CSS color, or gradient |
| `border` | Border color | — | Hex or CSS color |
| `stroke` | Section divider color | — | Hex or CSS color |
| `ring` | Ring color around current streak | — | Hex or CSS color |
| `fire` | Fire icon color | — | Hex or CSS color |
| `currStreakNum` | Current streak number color | — | Hex or CSS color |
| `sideNums` | Side numbers color | — | Hex or CSS color |
| `currStreakLabel` | Current streak label color | — | Hex or CSS color |
| `sideLabels` | Side labels color | — | Hex or CSS color |
| `dates` | Date text color | — | Hex or CSS color |
| `date_format` | Custom date format | locale | See [Date Formats](#-date-formats) |
| `locale` | Language for labels | `en` | ISO 639-1 code |
| `short_numbers` | Shortened numbers (e.g. 1.5k) | `false` | `true` / `false` |
| `type` | Output format | `svg` | `svg`, `png`, `json` |
| `mode` | Streak counting mode | `daily` | `daily` or `weekly` |
| `exclude_days` | Days to exclude from streak | — | `Sun,Sat` |
| `disable_animations` | Turn off animations | `false` | `true` / `false` |
| `card_width` | Card width in pixels | `495` | Any positive integer |
| `card_height` | Card height in pixels | `195` | Min `170` |
| `hide_total_contributions` | Hide total section | `false` | `true` / `false` |
| `hide_current_streak` | Hide current streak | `false` | `true` / `false` |
| `hide_longest_streak` | Hide longest streak | `false` | `true` / `false` |
| `starting_year` | Contributions start year | account creation | Integer ≥ `2005` |

---

## 🖌️ Themes

Add `&theme=THEME_NAME` to your URL:

```md
[![GitHub Streak](https://streak-stats.demolab.com/?user=shahrozraza205-source&theme=dark)](https://github.com/shahrozraza205-source)
```

| Theme | Preview |
|:-----:|:-------:|
| `default` | ![default](https://i.imgur.com/IaTuYdS.png) |
| `dark` | ![dark](https://i.imgur.com/bUrsjlp.png) |
| `highcontrast` | ![highcontrast](https://i.imgur.com/ovrVrTY.png) |
| **More themes!** | 🎨 [View all available themes](./docs/themes.md) |

> Have a new theme idea? Share it via [Issue #32](https://github.com/DenverCoder1/github-readme-streak-stats/issues/32)!

---

## 📅 Date Formats

When `date_format` is not set, the format is auto-detected from your `locale`. To customize, use [PHP date format characters](https://www.php.net/manual/en/datetime.format.php). Wrap the **year part** in `[ ]` — it will be hidden when it matches the current year.

| Format String | Past Year Output | Current Year Output |
|:-------------:|:----------------:|:-------------------:|
| `d F[, Y]` | `14 April, 2020` | `14 April` |
| `j/n/Y` | `14/4/2020` | `14/4/2024` |
| `[Y.]n.j` | `2020.4.14` | `4.14` |
| `M j[, Y]` | `Apr 14, 2020` | `Apr 14` |

**Full customization example:**

```md
[![GitHub Streak](https://streak-stats.demolab.com/?user=shahrozraza205-source&currStreakNum=2FD3EB&fire=pink&sideLabels=F00&date_format=[Y.]n.j)](https://github.com/shahrozraza205-source)
```

---

## 🗪 Locales

Supports **60+ languages**. The `locale` parameter accepts any ISO 639-1 code.

| Code | Language | Code | Language |
|:----:|:--------:|:----:|:--------:|
| `en` | English | `ur_PK` | اردو (پاکستان) |
| `ar` | العربية | `pa` | ਪੰਜਾਬੀ |
| `hi` | हिन्दी | `zh_Hans` | 中文（简体） |
| `fr` | Français | `de` | Deutsch |
| `ja` | 日本語 | `ko` | 한국어 |
| `es` | Español | `ru` | Русский |
| `tr` | Türkçe | `pt_BR` | Português (Brasil) |

[View full locale list and translation progress ➜](https://github.com/DenverCoder1/github-readme-streak-stats/blob/main/src/translations.php)

> Want to help translate? See [Issue #236](https://github.com/DenverCoder1/github-readme-streak-stats/issues/236).

---

## ℹ️ How Stats Are Calculated

This tool reads your **public GitHub contribution graph** to compute stats:

| Stat | How It's Counted |
|:----:|:----------------:|
| **Total Contributions** | All commits, pull requests, and issues in standalone repos |
| **Current Streak** | Consecutive days up to today (or yesterday if no contribution yet today) |
| **Longest Streak** | Highest ever number of consecutive contribution days |

> 🔒 To include **private repo contributions**, enable *"Private contributions"* in the dropdown above your GitHub contribution graph.

> ⏳ New contributions may take **up to 24 hours** to appear. [Learn why ➜](https://docs.github.com/articles/why-are-my-contributions-not-showing-up-on-my-profile)

---

## 📤 Self-Hosting

Host your own instance for better uptime and full customization. Supports **Vercel (free)**, **Heroku (paid)**, **Docker**, and manual PHP server deployment.

---

### ▲ Vercel — Free & Recommended

> PNG output is not supported on Vercel, but SVG (default) works perfectly.

[![Deploy with Vercel](https://i.imgur.com/Mb3VLCi.png)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FDenverCoder1%2Fgithub-readme-streak-stats%2Ftree%2Fvercel&env=TOKEN&envDescription=GitHub%20Personal%20Access%20Token%20(no%20scopes%20required)&envLink=https%3A%2F%2Fgithub.com%2Fsettings%2Ftokens%2Fnew%3Fdescription%3DGitHub%2520Readme%2520Streak%2520Stats&project-name=streak-stats&repository-name=github-readme-streak-stats)

📺 [Watch the video tutorial](https://www.youtube.com/watch?v=maoXtlb8t44)

<details>
<summary><b>📖 Step-by-step Vercel instructions</b></summary>

> ⚠️ Deploy from the **`vercel` branch**, not `main`.

1. Click **Deploy with Vercel** above
2. Enter a repo name and click **"Create"**
3. Generate a GitHub Personal Access Token at [this link](https://github.com/settings/tokens/new?description=GitHub%20Readme%20Streak%20Stats) (no scopes needed)
4. Add environment variable: key `TOKEN`, value = your token
5. Click **"Deploy"** — your domain replaces `streak-stats.demolab.com` in the URL

> Optionally set `WHITELIST=shahrozraza205-source` to restrict access to your username only.

</details>

---

### 🟣 Heroku — All Features (Paid ~$5–7/month)

Supports all features including **PNG rendering with Inkscape**.

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/DenverCoder1/github-readme-streak-stats/tree/main)

<details>
<summary><b>📖 Step-by-step Heroku instructions</b></summary>

1. Sign in at [heroku.com](https://heroku.com)
2. Generate a GitHub token at [this link](https://github.com/settings/tokens/new?description=GitHub%20Readme%20Streak%20Stats)
3. Click **Deploy to Heroku** above
4. Add Config Var: key `TOKEN`, value = your token
5. Optionally add `WHITELIST=shahrozraza205-source`
6. Click **"Deploy App"** — live at `<your-app-name>.herokuapp.com`

</details>

---

### 🐳 Docker — Full Control

```bash
# Clone the repo
git clone https://github.com/shahrozraza205-source/github-readme-streak-stats.git
cd github-readme-streak-stats

# Build the image
docker build -t streak-stats .

# Run (replace YOUR_TOKEN with your GitHub Personal Access Token)
docker run -d -p 8080:80 -e TOKEN=YOUR_TOKEN streak-stats

# Optional: restrict to your username only
docker run -d -p 8080:80 -e TOKEN=YOUR_TOKEN -e WHITELIST=shahrozraza205-source streak-stats
```

Visit `http://localhost:8080` to access your instance.

---

### 🌐 Manual Server Deployment

Transfer files to any PHP-enabled web server via FTP or SSH. See [CONTRIBUTING.md](./CONTRIBUTING.md) for full installation steps.

---

## 🤝 Contributing

Contributions are always welcome! Here's how to get involved:

- 🐛 [Open an issue](https://github.com/shahrozraza205-source/github-readme-streak-stats/issues/new/choose) for bugs or feature requests
- 🎨 Contribute a new theme via [Issue #32](https://github.com/DenverCoder1/github-readme-streak-stats/issues/32)
- 🌍 Help translate via [Issue #236](https://github.com/DenverCoder1/github-readme-streak-stats/issues/236)
- 📥 Submit a [pull request](https://github.com/shahrozraza205-source/github-readme-streak-stats/compare) with improvements

Please test the app locally before submitting a PR. See [CONTRIBUTING.md](./CONTRIBUTING.md) for full guidelines.

---

## 💙 Support

If this project helped you, please give it a ⭐ and share it with fellow developers!

[![YouTube](https://img.shields.io/badge/-Subscribe-red?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCipSxT7a3rn81vGLw9lqRkg?sub_confirmation=1)
[![Sponsor](https://img.shields.io/badge/-Sponsor-ea4aaa?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sponsors/DenverCoder1)
[![Ko-fi](https://img.shields.io/badge/-Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=ko-fi&logoColor=black)](https://ko-fi.com/jlawrence)

---

<div align="center">

Made with ❤️ and PHP

[![Powered by Heroku](https://img.shields.io/badge/-Powered%20by%20Heroku-6567a5?style=for-the-badge&logo=heroku&logoColor=white)](https://heroku.com/)

**[⬆ Back to Top](#-github-readme-streak-stats)**

</div>
