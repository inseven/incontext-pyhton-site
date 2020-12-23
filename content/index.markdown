---
title: InContext
template: page.html
category: pages
---

Most existing static site generators do a great job with text content, but treat media as an afterthought. InContext handles Markdown just as well as generators like [Jekyll](https://jekyllrb.com/), and adds native support for photos and video. Adding support for additional media types is simply a matter of adding a new handler.

# Getting Started

1. [Install Docker](https://docs.docker.com/engine/install/)
2. Clone the repository:

   ```bash
   git clone git@github.com:inseven/incontext.git
   ```
   
3. Add InContext to your path:

   ```bash
   export PATH=$PATH:/path/to/incontext
   ```

4. Create and build a new site:

   ```bash
   incontext new my-new-site
   cd my-new-site
   incontext build
   ```

# Documentation

You can find documentation [here](docs).

# Design Principles

To keep things simple, InContext follows some basic design principles:

- No media type is more important than any other; images are just as important as text, as video, etc.
- Every URL has a corresponding file backing it in the content directory of the site.

# Contributing

InContext is open source and we're always happy to receive contributions.

Check out the [open issues](https://github.com/inseven/incontext/issues) for somewhere to start.
