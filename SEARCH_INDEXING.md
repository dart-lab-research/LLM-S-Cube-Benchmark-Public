# Google Search indexing setup

GitHub Pages publishes the `docs/` directory on the `main` branch. Files in the repository root are not served at the project website root.

## Published files

- Homepage: https://dart-lab-research.github.io/LLM-S-Cube-Benchmark-Public/
- Google verification: https://dart-lab-research.github.io/LLM-S-Cube-Benchmark-Public/google73a00dde3e976afa.html
- Sitemap: https://dart-lab-research.github.io/LLM-S-Cube-Benchmark-Public/sitemap.xml

Keep `docs/google73a00dde3e976afa.html` unchanged and available after verification. Its contents must match the file supplied by Google. The homepage uses the full paper title and a self-referencing canonical URL. The sitemap lists only the public homepage, not verification files or repository implementation files.

## Complete in Google Search Console

1. Open https://search.google.com/search-console/ using the Google account that supplied the verification file.
2. Add or select the URL-prefix property `https://dart-lab-research.github.io/LLM-S-Cube-Benchmark-Public/` (including the trailing slash).
3. Choose HTML file verification. Once the verification URL above serves the supplied file, click Verify.
4. Use URL Inspection on the homepage, review the reported indexing status, and run Test Live URL. If eligible, request indexing.
5. In Sitemaps, submit `https://dart-lab-research.github.io/LLM-S-Cube-Benchmark-Public/sitemap.xml`.
6. Check URL Inspection again later. Successful deployment, verification, and a live test do not guarantee indexing or a particular search ranking.

No Search Console verification, sitemap submission, or indexing request is performed merely by deploying these files. Those actions must be completed in the account UI.

## Project naming

Use `LLM-S³ (LLM S Cube) Benchmark` as the visible project name, `LLM-S3` as the plain-text spelling, and retain the full paper title. The homepage and README explain that these names refer to the same project. Use natural wording instead of hidden keyword lists or repeated query variations; Google determines query matching and ranking after crawling.

## Maintenance

- Publish homepage changes through `docs/` on `main`.
- Keep the canonical URL and sitemap consistent if the public URL changes.
- Add sitemap entries only for real public pages. No fabricated modification dates are included.
- A `robots.txt` in this project's `docs/` would be served under the project path; crawler rules must instead be hosted at the origin root `https://dart-lab-research.github.io/robots.txt`. This change does not create a project-level robots file.
- Preserve links to the homepage from the repository README and relevant author or laboratory pages.

## References

- [Verify site ownership](https://support.google.com/webmasters/answer/9008080)
- [Request recrawling](https://developers.google.com/search/docs/crawling-indexing/ask-google-to-recrawl)
- [Build and submit a sitemap](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap)


## Search favicon and site-name scope

The project has an AI-generated survey respondent favicon in ICO and PNG formats; its title starts with `LLM-S3 Benchmark` and retains the full paper title. These files improve browser identification and provide a stable icon for reuse.

Google supports one search favicon and one site name per hostname, not per project subdirectory. The root `https://dart-lab-research.github.io/` returned HTTP 404 on 2026-09-14. Adding icons or `WebSite` site-name data only to this project's subdirectory cannot fully configure the host-level search identity.

An organization maintainer should publish an appropriate organization homepage in `dart-lab-research/dart-lab-research.github.io`, link its favicon from the root homepage, and add `WebSite` structured data there. The name and icon will represent all projects under that host and should be agreed at organization level. A prepared starter uses the proposed label “DART Lab Research”; it has not been deployed by this project change.

Repository administrators can also set the repository About description to:

> LLM-S3 (LLM S Cube) Benchmark: evaluating large language models as virtual survey respondents. Official code, datasets, and project page.

Suggested repository topics: `llm-s3`, `llm-s-cube`, `benchmark`, `survey-simulation`, `large-language-models`. The current collaborator has push access but no admin access; repository About settings are not changed by this commit.

Names and metadata are signals, not guarantees of Google selection or query ranking. Keep the established URL and consistent project aliases; avoid repeated keyword lists or frequent renaming.

- [Google favicon requirements](https://developers.google.com/search/docs/appearance/favicon-in-search)
- [Google site-name requirements](https://developers.google.com/search/docs/appearance/site-names)

The final logo combines three respondent silhouettes with a checked survey speech bubble. Source artwork: `docs/assets/llm-s3-survey-logo.png`; generation prompt: `branding/logo-generation.txt`. The earlier geometric cube icon has been replaced.
