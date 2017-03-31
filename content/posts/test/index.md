---
layout: Post
title: Referencing images in markdown
date: 2017-03-31
description: "Testing relative images in markdown"
---

# Technique used on putaindecode.io

![test](test.jpg)

Following the guidence here: [Referencing images in markdown](https://github.com/MoOx/phenomic/issues/731)

1) Added this file-loader to webpack:

```
  {
    test: /content(\/|\\).*\.(html|json|txt|ico|jpe?g|png|gif)$/,
    loader: "file-loader" +
      "?name=[path][name].[ext]&context=" +
      path.join(config.cwd, config.source),
  },
```

2) Included an image in `/content/posts/test/test.jpg`

3) Linked it relatively in the markdown `![test](test.jpg)`