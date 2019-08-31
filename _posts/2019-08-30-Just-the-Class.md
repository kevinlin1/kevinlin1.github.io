---
layout: post
title: Just the Class
excerpt: >-
  A Jekyll template for developing course websites.
---

See the template live with [Data 100][] offered at UC Berkeley and [CSE 373][]
offered at the University of Washington.

[Data 100]: http://www.ds100.org/fa19/
[CSE 373]: https://courses.cs.washington.edu/courses/cse373/19au/

## About [Just the Class][]

[Just the Class]: /just-the-class/

**[Just the Class][]** is a GitHub Pages template developed for
the purpose of quickly deploying course websites. In addition to serving plain
web pages and files, it provides a boilerplate for:

- a [course calendar](/just-the-class/calendar/)
- a [staff](/just-the-class/staff/) page
- a weekly [schedule](/just-the-class/schedule/)
- and posting [announcements](/just-the-class/announcements/).

Just the Class is built on top of [Just the Docs][], making it easy to extend
for your own special use cases while providing sane defaults for most
everything else. This means that you also get:

[Just the Docs]: https://github.com/pmarsceill/just-the-docs

- automatic [navigation structure][],
- instant, full-text [search][] and page indexing,
- and a small but powerful set of [UI components][] and authoring [utilities][].

[navigation structure]: https://pmarsceill.github.io/just-the-docs/docs/navigation-structure/
[search]: https://pmarsceill.github.io/just-the-docs/docs/search/
[UI components]: https://pmarsceill.github.io/just-the-docs/docs/ui-components
[utilities]: https://pmarsceill.github.io/just-the-docs/docs/utilities

## Course Website as a One-Stop Shop

One neat feature is the full-text [search][] capability. I use it to index all
of the content in the course, including PDF-based materials such as lecture
slides and section handouts. Try searching the [CSE 373][] course website for
terms like "abstract data types" or "TMWLO" and you'll see it pick up uses
from lecture.

If you click through one of the lecture search results, you'll notice that it
brings you briefly to a redirect landing page. When generating the website on
the backend, this page is picked up and treated as any other page. When visited
by the web browser, the page redirects to the content. Here's what to do to get
this behavior.

### Modify the template

1. In your website repository, create a file `_includes/head_custom.html`. This
   will overwrite the [blank file][] provided by the website theme.

2. Add the following lines to the file.
   {% raw %}
   ```html
   {% if page.redirect_to %}
   <style>body { display: none; }</style>
   <meta http-equiv="refresh" content="0; url={{ page.redirect_to }}">
   {% endif %}
   ```
   {% endraw %}

### Add a placeholder content page

1. If you're adding a lecture, for example, create a file `lectures/01.md`.

2. Add the following [front matter][] to the newly-created file, where the
   `title` is whatever you'd like it to be titled and the URL is your redirect.
   ```markdown
   ---
   title: Welcome to CSE 373
   nav_exclude: true
   redirect_to: &redirect https://docs.google.com/presentation/d/1w9sZhSH6MPBh_WB9dcBuz5RSUE32GqBcCXo6jprVQwI/edit#usp=sharing
   canonical_url: *redirect
   ---
   ```

3. In the body of the newly-created file, copy and paste in your plain-text
   content. I use Google Slides for lecture which can be downloaded as a `txt`.

[blank file]: https://github.com/pmarsceill/just-the-docs/blob/master/_includes/head_custom.html
[front matter]: https://jekyllrb.com/docs/front-matter/
