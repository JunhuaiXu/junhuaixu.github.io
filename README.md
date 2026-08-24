# Junhuai Xu Academic Website

Public site: <https://junhuaixu.github.io>

## Content ownership

- Cross-application facts: `../../06_Profile_Master/canonical_facts.yaml`
- Academic CV master: `../../00_Academic_Master/01_CV_Master/`
- Publication-list master: `../../00_Academic_Master/02_Publication_List_Master/`
- Research-statement master: `../../00_Academic_Master/03_Research_Statement_Master/`
- Website pages: `_pages/`
- Website-specific images: `assets/images/`
- Downloadable PDFs: `assets/files/`

Shared facts and academic documents should be updated in their master locations first, then synchronized to
`assets/files/`. Role-specific applications, unpublished claims, immigration strategy, and application status do
not belong on the public website.

## Public entry points

- `/`: research overview, experiments, news, education, awards, and downloads
- `/publications/`: selected first-author publications and complete-record links
- `/cv/`: current CV, publication list, and research statement
- `/research/...`: physics research pages
- `/ai/...`: public computational-method pages
- `/experiments/...`: detector and beam-test pages

Historical Academic Pages template examples remain in the repository for provenance but are excluded from the
public build in `_config.yml`.

## Maintenance checks

Before publishing:

1. compare public claims with the academic masters and claim guardrails;
2. compile PDFs outside `assets/files/` and copy back only the final PDFs;
3. check `git diff --check` and confirm no `.aux`, `.log`, or `.out` files are staged;
4. verify local links, downloadable files, desktop layout, and mobile layout;
5. commit and push the website as a standalone change.
