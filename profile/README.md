<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/wordmark-transparent-light-text.png">
    <img alt="limbo.watch" src="assets/wordmark-transparent-dark-text.png" width="400">
  </picture>
</p>

<p align="center"><b>Published. Not reviewed. Not scanned. In limbo.</b></p>

When a maintainer publishes a security advisory in their GitHub repository, Dependabot, npm audit, OSV-Scanner and most dependency scanners can't see it until GitHub reviews it into the global Advisory Database. That takes weeks. Until then, the advisory is **in limbo**: public, usually already fixed, and invisible to the tools teams rely on.

**Limbowatch** measures that gap in the open, and closes it in your CI.

- 🌐 **[limbo.watch](https://limbo.watch)**: the live tracker. Every advisory in limbo across about 18,600 watched repos, re-checked daily.
- 🔎 **[Scan your project](https://limbo.watch/scan/)**: `limbowatch scan` checks your lockfiles against every advisory in limbo and reports in GitLab merge requests, GitHub pull requests and Gitea/Forgejo issues. On a demo app it found 16 advisories that neither OSV-Scanner nor Dependabot reported ([see the pull request](https://github.com/limbowatch/demo-app/pull/1)).
- 📦 **[The limbo feed](https://limbo.watch/feed/)**: every advisory in limbo as OSV records, rebuilt daily. The released OSV-Scanner can scan against it today.
- 📊 **[State of the Gap, October 2026](https://github.com/limbowatch/limbowatch/tree/main/research/2026-10-state-of-the-gap)**: 1 in 6 upstream advisories of 15 popular projects was in limbo; 13 of 14 projects shipped affected versions their scanner reported as clean.

Source: [limbowatch/limbowatch](https://github.com/limbowatch/limbowatch) · GitLab CI/CD component: [gitlab.com/limbowatch/limbowatch-component](https://gitlab.com/limbowatch/limbowatch-component)

Open source (Apache-2.0); research data and the feed are CC BY 4.0.
