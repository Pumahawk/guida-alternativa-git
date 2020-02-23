---
layout: wiki
title: Hot to make a guide
previus_doc: /docs/stepbystep/Intro.html
breadcrumb:
  - /guides/stepbystep
---
A guide is only a series of documents connected together.

To make a guide, first you create a file `/_guides/myguide.md`. Initialize it adding
this line:

```markdown
---
layout: guide
title: My guide title
docs:
 - /docs/id/of/my/doc
 - /docs/id/of/my/second/doc
--- 
Hi this is my first guide!
```

Now you have your first guide!