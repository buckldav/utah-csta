---
sidebar_position: 2
---

# Contributing

## How to add a Blog Post

1. Fork [this repository](https://github.com/buckldav/utah-csta).
2. Add a page under the `/blog/` folder with the format `YYYY-MM-DD-title.md`.
3. Add the following to your new page:

```markdown title="Put at the top of your Markdown file."
---
slug: path-to-post
title: Post Title
authors: [yourName]
tags: [tag1, tag2]
---

your article goes here...
```

4. Modify `/blog/authors.yml` to contain your info:

```yaml title="authors.yml"
buckley:
  name: David Buckley
  title: CS Teacher - Merit Academy
  url: https://github.com/buckldav
  image_url: https://github.com/buckldav.png

yourName:
  name: Your Name
  title: CS Teacher - Your School
  url: https://github.com/<username>
  image_url: https://github.com/<username>.png
```

5. Commit change and submit a pull request.
