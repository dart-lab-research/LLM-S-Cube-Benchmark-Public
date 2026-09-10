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
