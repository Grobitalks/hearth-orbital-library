# Hearth Orbital Library

A reading copy of 1,500 public-domain books, split into small plain-text page files so that a VRChat world can load and
show them with VRChat's string loader. It's a non-commercial project.

## Where the texts come from

The texts come from [Project Gutenberg](https://www.gutenberg.org/), the free library of public-domain e-books, and we're
grateful to its volunteers. Each book was downloaded once through Project Gutenberg's own mirror. The Project Gutenberg header,
footer and licence, and every other mention of Project Gutenberg, were removed from the text files, as the Project Gutenberg
licence asks when texts are redistributed in a changed form. So these files are **not Project Gutenberg eBooks**, and they are
not endorsed by Project Gutenberg. To read the originals, or for e-book formats, visit gutenberg.org.

All the texts are in the **public domain in the United States**. Copyright laws differ between countries; if you are
outside the United States, check your local laws before you use these texts.

## Layout

- `catalog.json`: the list of books: `id` (the Project Gutenberg number), `t` title, `a` author, `l` language, `s` shelf,
  `sub` subjects, `p` pages, `c` chunk files, `r` popularity rank.
- `b/<id>/<n>.txt`: chunk `n` of book `id`, UTF-8. Records are separated by a form feed (`\f`). Record 0 is a header:
  `HOLB1 <id> <chunk> <firstPage> <pagesInChunk> <totalPages> <contentsCount>` (tab-separated), followed by the contents
  lines (`<page>\t<label>`). Each later record is one page, about 1,500 to 1,900 characters, in TextMesh Pro rich text (only
  `<i>` and `<b>`). There are 80 pages in a chunk, so page `p` is in chunk `p / 80`.

1,500 books, 7,316 chunk files.
