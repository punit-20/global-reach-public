# Contributing to Global Reach (Public Portal & Documentation)

Thank you for helping improve the Global Reach documentation, website accessibility, and community resources.

## Scope of This Repository

This public repository contains only the static website, user documentation, legal policy pages, and issue templates. Application service code is maintained separately from this public documentation repository.

## How to Contribute

1. **Report Bugs:** Use the [Bug Report template](https://github.com/punit-20/global-reach-public/issues/new?template=bug_report.yml).
2. **Suggest Enhancements:** Use the [Feature Request template](https://github.com/punit-20/global-reach-public/issues/new?template=feature_request.yml) or start a thread in [GitHub Discussions](https://github.com/punit-20/global-reach-public/discussions).
3. **Documentation & Website Fixes:**
   - Keep all internal HTML/CSS/asset paths relative (`./` or `../`) so the site works on GitHub Pages project subpaths (`/global-reach-public/`).
   - Maintain WCAG contrast and keyboard focus outlines (`:focus-visible`).
   - Do not introduce external JavaScript frameworks or tracking scripts.

## Strict Security Rule

**Never commit or paste:**
- Discord application tokens, personal tokens, or HTTP `Authorization` headers
- Configuration secrets or session cookies
- Personal Discord User IDs, Server IDs, or community member lists
