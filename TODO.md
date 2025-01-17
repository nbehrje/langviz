# TODO

This document contains items on the immediate horizon. Check the README for a list of implemented and planned features.

---

## General

- After optimizations, update examples in examples dir

- Add status update terminal messages

- Organize the argparse and argument access code blocks

## Optimization

- Experiment with spaCy model sizes (processing time VS accuracy), and using DocBin to create the cache if the pickle gets too large

- Bertopic: instead of using sentence transformers, maybe use spaCy vectors since they're already generated
-
- Make each component non-blocking: the application shouldn't have to wait for each component to finish,
  it will instead show a loading bar for each. `dcc.Loading` may take care of this, otherwise will need to use asynchronous functions

- Experiment with saving cache to user's home dir (or wherever caches are typically saved)

## Debugging

- Debug document frequency issues (<10 documents, bertopic acts up. Below idea will solve this issue)
- Make it so if a components fails to complete, it will just show an error in that region of the app, instead of throwing an exception
