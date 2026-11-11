<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/wordmark-transparent-light-text.png">
    <img alt="limbo.watch" src="assets/wordmark-transparent-dark-text.png" width="400">
  </picture>
</p>

<p align="center"><b>Security advisories your scanner can't see yet.</b></p>

When maintainers publish a security advisory in their GitHub repository, it doesn't reach the GitHub Advisory Database or OSV until GitHub reviews it. Dependabot, npm audit, OSV-Scanner and most dependency scanners read those databases, so they stay silent in the meantime, often for weeks. The advisory is public and usually already fixed, but it's **in limbo**.

Limbowatch measures that gap in the open and closes it in CI.

### Projects

| | |
|---|---|
| **[Live tracker](https://limbo.watch)** | Every advisory in limbo across more than 60,000 watched upstream repositories, with how long each has waited and whether it has a CVE. Updated daily. |
| **[Watcher](https://limbo.watch/scan/)** | `limbowatch scan` checks a project's lockfiles or SBOM against advisories in limbo. Reports in GitLab merge requests, GitHub pull requests and Gitea or Forgejo issues, in ten formats including SARIF and CycloneDX. |
| **[Package checker](https://limbo.watch/check/)** | Type a package from npm, PyPI, crates.io or Maven: your browser checks it and its whole dependency tree against the advisories in limbo. |
| **[Limbo feed](https://limbo.watch/feed/)** | Every advisory in limbo as OSV records, rebuilt daily. OSV-Scanner can scan against it today. |
| **[State of the Gap](https://github.com/limbowatch/limbowatch/tree/main/research/2026-10-state-of-the-gap)** | October 2026 research. About 1 in 6 upstream advisories of 15 popular projects was in limbo, and 13 of 14 projects shipped affected versions their scanner reported as clean. |

### Get started

```yaml
# GitLab CI/CD
include:
  - component: $CI_SERVER_FQDN/limbowatch/limbowatch-component/limbowatch@0.1.0-alpha.8
```

```yaml
# GitHub, Gitea or Forgejo Actions
- uses: limbowatch/limbowatch-action@v0.1.0a8
  with:
    fail-on: high
```

```sh
# Anywhere else
docker run --rm -v "$PWD:/src" ghcr.io/limbowatch/limbowatch:0.1.0a8 limbowatch scan .
pipx install limbowatch-cli==0.1.0a8
```

The action is in [GitHub Marketplace](https://github.com/marketplace/actions/limbowatch) and the component in the [GitLab CI/CD Catalog](https://gitlab.com/explore/catalog/limbowatch/limbowatch-component). Releases are alphas: options and formats may change before 0.1.0.

### Links

[Source](https://github.com/limbowatch/limbowatch) · [Documentation](https://github.com/limbowatch/limbowatch/blob/main/docs/WATCHER.md) · [Methodology](https://limbo.watch/methodology/) · [GitHub Marketplace](https://github.com/marketplace/actions/limbowatch) · [GitLab CI/CD Catalog](https://gitlab.com/explore/catalog/limbowatch/limbowatch-component) · [PyPI](https://pypi.org/project/limbowatch-cli/) · [Security policy](https://github.com/limbowatch/limbowatch/blob/main/SECURITY.md) · [Press](https://limbo.watch/press/)

Open source under Apache-2.0. Research data and the feed are CC BY 4.0. Advisory data comes from GitHub repository security advisories and the GitHub Advisory Database (CC BY 4.0).
