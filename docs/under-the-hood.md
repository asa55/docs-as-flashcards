---
layout: default
title: Under the hood
nav_order: 2
---

## Under the hood

As mentioned on the homepage, the [`*-docs-as-flashcards` project](https://asa55.github.io/docs-as-flashcards/) makes flashcards compatible with the [Anki flashcard app](https://github.com/ankitects/anki). All [`*-docs-as-flashcards` projects](https://asa55.github.io/docs-as-flashcards/) accept markdown (`.md` files) as input, and generate Anki-compatible flashcard decks (`.apkg` files) as output. 

The engine that does this is called [`md2apkg`](https://github.com/Steve2955/md2apkg) that I did not write, wrapped in a GitHub Actions workflow I wrote ([`md2apkg-run`](https://github.com/asa55/md2apkg-run)) so that GitHub can do the heavy lifting associated with the conversion process.

## Considerations

The [`*-docs-as-flashcards`](https://asa55.github.io/docs-as-flashcards/) and [`md2apkg-run`](https://github.com/asa55/md2apkg-run) projects are not affiliated with (but grateful to) the [`md2apkg` project](https://github.com/Steve2955/md2apkg) and the [Anki project](https://github.com/ankitects/anki).

Of all the flashcard apps out there, [Anki](https://github.com/ankitects/anki) was selected to be leveraged by the [`*-docs-as-flashcards` project](https://asa55.github.io/docs-as-flashcards/) because it's extremely popular with a great community, free, open-source, and easy do download for desktop and mobile.

Of all the conversion tools that convert different inputs to Anki, [`md2apkg`](https://github.com/Steve2955/md2apkg) was selected because the syntax is simple. The flashcard definition `.md` files are very human-readable, which makes maintenance and new contributions a breeze. I didn't want to suffer a learning curve every time I decide to update or contribute new flashcards in the future. `md2apkg` makes this easy imho.
