# viral post studio

a small tool that turns a topic into an X post or thread using formats that actually get reach in 2026. pick single post or thread, pick a template, drop in your specifics, copy it out.

live version: https://jyoti369.github.io/viral-post-studio/

## why it exists

most post generators spit out stuff that reads like a bot wrote it. em dashes everywhere, words like "seamless" and "robust", the works. this one is built the other way round. the copy is written in a normal voice, and there's a guard that strips em dashes and flags robot words before anything even reaches the preview.

## what's inside

- single posts and threads, 12 templates grouped by goal: hot take, before/after proof, listicle, how-to, question, launch, hiring, plus story, contrarian and case-study threads
- a reach signal score out of 100 that grades each post against how X actually ranks in 2026. replies count far more than likes, links belong in the first reply not the post, no all-caps, and so on
- everything in the preview is editable, so you fix it in your own voice before posting
- copy per post or the whole thread at once, dark and light, works on your phone

## run it

it's a single file with no build step and no dependencies. just open `index.html` in a browser, or use the hosted link above.

## adding your own templates

the hiring template is the exact format from a post that worked well: bracketed headline, bullet skills, arrow work-includes, link kept out of the post. to add your own, edit the `SINGLE` and `THREAD` arrays near the top of the script in `index.html`. each template is a small object with an `id`, a `name`, a `goal`, a short `why` note, the input `fields` it needs, and a `build` function that returns a string for a single post or an array of strings for a thread.
