# Blog

### Install

```bash
git submodule update --init --recursive
```

or 

```bash
git submodule update --remote --merge
```

### Deploy

1. Build static pages

```bash
hugo -d build
```

2. Make sure git knows about your subtree (the subfolder with your site).

```bash
git add build && git commit -m "Algoclub release #1"
```

3. Use subtree push to send it to the `build` branch on GitHub.

```bash
git subtree push --prefix dist origin gh-pages
```

or use simple script:

```bash
git pages-deploy path/to/your/site version
```
