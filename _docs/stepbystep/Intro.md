---
layout: wiki
title: Step by step
next_doc: /docs/stepbystep/Make Guide
breadcrumb:
  - /guides/stepbystep
---

Completed [installation guide]({{"/guides/install.html" | relative_url}}) you can learn how to make 
you firt documentation.

We can begin with a simple documentation.

## Create one page

To write a single documentation you only need to create a file in `/_docs` folder
and link it in home.

For exemple imagine that you want to create a documentation called "_How to make it_".
Create a file `/_docs/How to make it.md`. Initialize it adding this following line 
at the begin of the file.

```markdown
---
layout: wiki
title: How to make it
---
```

Now write your content in __markdown__ like this.

```markdown
---
layout: wiki
title: How to make it
---

# How to make it

To make it, first, make it!
```

Link it in home editing e simple config file `/_data/home.yml` like this.

```yml
intro: 
  output: true
  id: /docs/basic/Intro
```

Finally you have make your first documentation!

Continue to know _How to make a guide_.