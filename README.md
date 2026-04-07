# 📋 Weekly Report Generator

> AI-powered weekly report generator — aggregates your GitHub activity, tasks, and calendar into a polished weekly report.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-purple)](https://clawhub.ai/skills/weekly-report-fx)

## ✨ Features

- 🤖 **AI-Powered** — Uses AI to distill raw data into meaningful insights
- 📊 **GitHub Integration** — Scans issues, PRs, and commits automatically
- 📅 **Calendar Ready** — Works with Feishu Calendar (more integrations coming)
- ✅ **Task Tracking** — Pulls completed tasks from Reminders or Things 3
- 🎨 **Multiple Styles** — Detailed, concise, or executive summaries
- 📄 **Multiple Formats** — Markdown, HTML, or plain text output
- 🔒 **Privacy First** — All data processed locally, nothing stored remotely

## 🚀 Quick Start

### As an OpenClaw Skill

Install via ClaWHub:

```bash
clawhub install weekly-report
```

Then ask OpenClaw:

```
"生成我的周报"
"Generate my weekly report for last week"
```

### Standalone CLI

```bash
# Install dependencies
npm install

# Run (this week's report)
npm start

# Run with options
npm start -- -w -1 -f html -s executive
```

## 📖 Usage

### Command Line Options

| Option | Description | Default |
|--------|-------------|---------|
| `-w, --week-offset <n>` | Week offset (0=this week, -1=last week) | `0` |
| `-f, --format <fmt>` | Output format: `markdown`, `html`, `plain` | `markdown` |
| `-s, --style <style>` | Report style: `detailed`, `concise`, `executive` | `detailed` |
| `-r, --repos <list>` | Comma-separated GitHub repos (owner/name,...) | auto-detect |
| `--dry-run` | Generate sample report without fetching data | false |

### Environment Variables

```bash
# Required for private repos
export GITHUB_TOKEN=ghp_your_token_here

# Optional Feishu integration
export FEISHU_APP_ID=your_app_id
export FEISHU_APP_SECRET=your_app_secret
```

## 📋 Sample Output

```markdown
# 📋 Weekly Report — Week 15

> **Generated:** April 7, 2026
> **Period:** April 7 → April 13, 2026

---

## 📊 Week at a Glance

| Metric | Count |
|--------|-------|
| 🔵 Issues Closed | 5 |
| 🟢 PRs Merged | 3 |
| 📝 Commits | 12 |

---

## 🚀 Accomplishments

### Pull Requests (3 merged)
- ✅ feat: add user dashboard `fx-world888/project` #45
- ✅ fix: resolve login redirect loop `fx-world888/project` #43
- ✅ refactor: clean up API endpoints `fx-world888/project` #41

### Issues Resolved (5)
- Fix authentication timeout bug
- Add dark mode support
- ...

---

## 🎯 Next Week's Goals

- [ ] Continue dashboard development
- [ ] Start user feedback implementation
- [ ] Review Q2 roadmap
```

## 🏗️ Architecture

```
weekly-report/
├── SKILL.md                      # OpenClaw skill definition
├── scripts/
│   └── generate-report.mjs       # Main report engine
├── examples/
│   └── sample-report.md          # Example output
└── README.md
```

## 🤝 Contributing

Contributions welcome! Please read the contribution guidelines first.

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/amazing`)
3. Commit your changes (`git commit -m 'feat: add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing`)
5. Open a Pull Request

## 📄 License

MIT © fx-world888

## 🙏 Acknowledgments

Published on [ClaWHub](https://clawhub.ai/skills/weekly-report-fx) — install with `clawhub install weekly-report-fx`

Built with [OpenClaw](https://github.com/openclaw/openclaw) — the AI gateway that makes building powerful skills easy.
