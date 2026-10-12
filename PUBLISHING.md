# Publishing this release repository

1. Create a **public** GitHub repository for releases, separate from private source.
2. If GitHub already contains an initial README, clone that repository into a new
   directory first. Copy this folder's documentation, `.gitignore`, `.gitattributes`
   and `docs/` into the clone. Do not copy or replace `.git`.
3. Commit the documentation and push. Do not upload the implementation source ZIP.
4. On GitHub, open Releases and draft a release tagged `v0.6.3` on `main`.
5. Title: `Political Engine 0.6.3`. Paste `RELEASE-v0.6.3.md` into the description.
6. Mark this experimental build as a pre-release. Attach both ZIPs from
   `release-assets/v0.6.3/` (plus `SHA256SUMS.txt` if desired).
7. Review author credits/resource permissions and dependencies before publishing.
8. Share the release page or individual archive download links.

`release-assets/` is Git-ignored on purpose. GitHub's automatic Source code ZIP
contains only documentation from this public repo, not the private mod code.
It is not an installable mod and should not be advertised as the download.

The installable mod necessarily ships runtime HTML/JavaScript and LLM prompts.
Those files can be inspected by downloaders. A private source repository protects
access to the full development project, not secrecy of every runtime component.

This folder has a local Git repository but no commits/remote/upload. Nothing has
been published automatically. Keep the source repository private separately.
