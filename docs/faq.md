---
layout: default
title: FAQ
nav_order: 4
---

# FAQ

Answers to questions nobody has ever actually asked me. So it's not false that these are all asked equally frequently.

## How does `*-docs-as-flashcards` work under the hood?

The [`*-docs-as-flashcards` project](https://asa55.github.io/docs-as-flashcards/) makes flashcards compatible with the [Anki flashcard app](https://github.com/ankitects/anki). All [`*-docs-as-flashcards` projects](https://asa55.github.io/docs-as-flashcards/) accept markdown (`.md` files) as input, and generate Anki-compatible flashcard decks (`.apkg` files) as output. 

The engine that does this is called [`md2apkg`](https://github.com/Steve2955/md2apkg) that I did not write, wrapped in a GitHub Actions workflow I wrote ([`md2apkg-run`](https://github.com/asa55/md2apkg-run)) so that GitHub can do the heavy lifting associated with the conversion process.

### Is this project affiliated with the Anki or `md2apkg` projects?

The [`*-docs-as-flashcards`](https://asa55.github.io/docs-as-flashcards/) and [`md2apkg-run`](https://github.com/asa55/md2apkg-run) projects are not affiliated with (but grateful to) the [`md2apkg` project](https://github.com/Steve2955/md2apkg) and the [Anki project](https://github.com/ankitects/anki).

### Why depend on Anki?

Of all the flashcard apps out there, [Anki](https://github.com/ankitects/anki) was selected to be leveraged by the [`*-docs-as-flashcards` project](https://asa55.github.io/docs-as-flashcards/) because it's extremely popular with a great community, free, open-source, and easy do download for desktop and mobile.

### Why depend on `md2apkg`?

Of all the conversion tools that convert different inputs to Anki, [`md2apkg`](https://github.com/Steve2955/md2apkg) was selected because the syntax is simple. The flashcard definition `.md` files are very human-readable, which makes maintenance and new contributions a breeze. I didn't want to suffer a learning curve every time I decide to update or contribute new flashcards in the future. `md2apkg` makes this easy imho.

### What if `md2apkg` or Anki end support? Will that be end of the `*-docs-as-flashcards` project?

Since the `md2apkg` syntax is so simple, this makes the flashcard definitions themselves only loosely coupled with `md2apkg`. I don't plan on changing engines any time soon, but writing an automation to make these flashcards compatible with another conversion engine or flashcard app should be pretty straightforward in theory. If either of the main dependencies were to lose support, `*-docs-as-flashcards` can be expected to continue support.

### Does `*-docs-as-flashcards` use all Anki features?

Anki is a powerful app. It offers many types of advanced flashcard formats (Cloze, for example). The ones used by `*-docs-as-flashcards` are the simplest of the simple; a single flashcard definition in `.md` corresponds to a single flashcard in Anki.

### Does `*-docs-as-flashcards` follow any writing / style conventions?

- Flashcards should be short and punchy; not open-ended
  - Each question has a terse and distinct answer
- One portion of the docs corresponds to one flashcard
  - I copy-paste the docs into a new `.md` file, split the concepts into distinct flashcards, and where necessary add context and arrange the wording so that it fits a Q&A format
  - This workflow ensures that the flashcard deck is comprehensive, and that the flashcard language mirrors the official docs as closely as possible
- Concepts are prioritized

### Does the double-colon (`::`) mean something special?

The double-colon (`::`) means something special within Anki, which is why it is used so heavily in the `*-docs-as-flashcards` projects. All nested tags in these projects are separated with a double-colon (`::`). Also, you can edit the names of decks within Anki (e.g. "MyDeck" for one, and "MyDeck::MySubDeck" for another) and Anki will automatically show these as nested decks within the app. It can be pretty convenient. There is also a popular "nested tags" extension for Anki Desktop. I don't believe it's available for mobile, but the tagging convention used in `*-docs-as-flashcards` will work nicely with it. Also, for those of us (i.e. mobile users) who can't download the nested tags extension, the `*-docs-as-flashcards` flashcards are also tagged with every tag in the nest, to simulate the benefit provided by the nested tags extension. (This is why for example a flashcard tagged with "Overview::About-Azure-Functions" is also tagged with just "Overview". If you filter for the "Overview" tag, you'll get to study everything nested inside with ease, even without downloading the nested tags extension).

### What is `md2apkg-run`?

It's a bonus gift for you 😄

`md2apkg-run` is a wrapper I wrote around `md2apkg` that automatically applies the right tags for all `*-docs-as-flashcards` projects, and of course you can use it too to create and tag your own Anki flashcards.

You too can generate your own custom Anki-compatible flashcard decks on GitHub without downloading any software or tooling to your device (except the Anki app itself and your custom flashcard deck). Complete instructions are provided on the [`md2apkg-run` project site](https://github.com/asa55/md2apkg-run)

### What are the limitations of `*-docs-as-flashcards`?

- Tutorials, how-to's, examples, samples, and so on are great! Just not for flashcards. The point of `*-docs-as-flashcards` is make it easier to pound information into your head so that you know all the pieces of the puzzle
  - There's this concept of Higher Order Thinking Skills, or HOTS ([Wikipedia link](https://en.wikipedia.org/wiki/Higher-order_thinking)) that makes sense (to me) when it comes to organizing my learning journey. Not that it's the way you like to think about it. But if you look at the linked image of Bloom's taxonomy, you'll see "remember" is the first step of the process. *Then* you get to understand, apply, analyze, evaluate, and create (i.e. write code using the concepts)
  - You can always use techniques other than (or in addition to) flashcards, but can't get around that first step
  - It's possible to make documentation about tutorials into flashcards, but at a certain point your time is better spent actually following the tutorials
  - I recommend getting all the little bits of information committed to memory with flashcards, then getting keyboard time by following up on all the other cool resources
  
