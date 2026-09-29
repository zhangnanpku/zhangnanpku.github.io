# Nan Zhang — al-folio website

This is a conversion of the supplied `website.zip` into the [al-folio](https://github.com/alshedivat/al-folio) Jekyll starter (source revision `40c0600`, MIT license; see `LICENSE`). It is configured for `https://zhangnanpku.github.io` at the domain root.

## Content

- `_pages/about.md`: biography, portrait, affiliation, contact, selected publications.
- `_bibliography/papers.bib`: 13 publications converted from the supplied research page. Update this single file to add papers; `selected = {true}` controls the home page selection. Author markers `*` and `†` were carried over from the old list.
- `_pages/teaching.md` and `_pages/DATA*.html`: teaching overview and three existing course outlines.
- `_pages/group.md`: graduate and undergraduate students.
- `_data/socials.yml`: email. Add verified Google Scholar, ORCID, and other profiles when ready.
- `assets/img/prof_pic.jpg`: existing portrait.

Legacy paths `/research/index-research.html` and `/teaching/index-teaching.html` have redirect pages. The `/cv/` page retains the original "available upon request" message. Two lecture video URLs in the original site had no files in the archive, so the topic names are retained without broken links.

## Publish to the existing GitHub Pages domain

1. Back up the current `zhangnanpku.github.io` repository, then place **the contents of this folder** at its root (including `.github/workflows/deploy.yml`).
2. Push to `main` or `master`. In repository Settings → Actions → General, allow workflow **read and write permissions**.
3. In Settings → Pages, choose **Deploy from a branch** and `gh-pages` / root. The al-folio deployment workflow builds the Jekyll site and publishes that branch.
4. Review the Actions build, then check `/`, `/research/`, `/teaching/`, `/group/`, and the three course links on desktop and mobile.

This changes the repository's site source. It has **not** been pushed or published. The build requires Ruby, Bundler, Node, and ImageMagick as configured in al-folio's workflow. The supplied archive contained no current CV PDF or lecture recordings. Academic details and student destinations should be reviewed before publication.
