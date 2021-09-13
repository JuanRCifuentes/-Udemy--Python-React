# Frontend Details

## Table of Contents
- [Frontend Details](#frontend-details)
  - [Table of Contents](#table-of-contents)
  - [Change Favicon and Title](#change-favicon-and-title)

## Change Favicon and Title

To change favicon, go to `index.html` and change line 27 to `<title>Images Gallery</title>`, and the description in line 10 to `content="Images Gallery Full-Stack Application"`

To generate favicon, go to [`favicon.io`](https://favicon.io). It will download a zip file with multiple files, including `site.webmanifest` (which mandates which icon use for each size).

Replace icons for the newly generated ones. Rename `site.webmanifest` to `manifest.json`. TIP: Format that file with Prettier to see multiple lines of code.

If the favicon doesn't change by then, empty cahces of your browser.