# lxl's changes

Added multiple-link lines, with or without title

line format in index.html:
Heading Text
http(s)://URL || Title || Name [ || Keybinding ]

1. if a line is empty/blank, it's skipped
2. if a line does NOT contain "://", it's a "Heading Text", which:
   - ends the current block of URLs if we are in one
   - starts a new block of URLs
3. if a line contains "://", it's a URL line with Title (required), Name (optional),
   and Keybinding (optional), separated by " || "
   - if Title is **NOT** "." and **NOT** "\_\_end\_\_", and Name is empty, the line starts a 1-URL
   - if Title is **NOT** "." and **NOT** "\_\_end\_\_", and Name is NOT empty, the line starts a multiple-URL
   - if Title is ".", and Name is **NOT** empty, the line continues current multiple-URL
   - if Title is "__end__", and Name is **NOT** empty, the line ends current multiple-URL

   see [index.html](index.html) for examples

# example site

Visit https://startpage-example.pages.dev/, hosted at Cloudflare pages, to see how current [index.html](index.html) works.

