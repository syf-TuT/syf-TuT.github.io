# Sailing Homepage Implementation Plan

**Goal:** Replace the minimal homepage with the approved personal site: sailing-photo profile panel and a minimal welcome area.

**Architecture:** Keep the existing static GitHub Pages site. Use semantic HTML and a single inline stylesheet, with local images and no JavaScript or build dependencies.

**Tech Stack:** HTML, CSS, local JPEG images.

## Approved design

- Desktop: a fixed profile panel occupying 35% of the viewport; a warm off-white reading area on the right.
- Use the supplied sailing photo as the profile background. Place the existing avatar, name, email, and repository-owner GitHub link above the boat.
- Right side: only `HELLO, I'M YUFAN`, the greeting `你好，欢迎来到我的page`, and the copyright. The user requested removal of the introduction and activity section after reviewing the first version.
- Shift the avatar image down inside its circular crop to show less neck (`object-position: center 10%`).
- Mobile: profile photograph above the content, with readable spacing and no horizontal scrolling.
- Quiet typography, sea-green accents, visible keyboard focus, and reduced-motion support.

## Implementation

1. Copy the supplied photo to `images/sailing.jpg` without altering it.
2. Update `index.html` with the profile aside, minimal welcome content, and responsive styles.
3. Review the code for unnecessary complexity. Keep all editable personal copy together in the HTML.
4. Serve locally and inspect desktop and mobile layouts in the browser. Verify images, link destinations, heading structure, and overflow; run `git diff --check`.

This is a reversible presentation change; browser verification is appropriate without adding a test framework. Leave changes in the current workspace for user review.
