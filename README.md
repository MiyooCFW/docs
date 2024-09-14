# MiyooCFW documentation pages (WIP)

### You can preview full docs, by running

- locally:
```
git submodule update --init --recursive
python3 -m mkdocs serve
```
- in the Web browser from a htmlpreview:
 [here](https://html-preview.github.io/?url=https://github.com/MiyooCFW/docs/blob/site-preview/index.html)

### Build with
```
python3 -m mkdocs build
```
### Publish for

- GitHub Pages:
```
python3 -m mkdocs gh-deploy --remote-branch site --no-history
```

- html-preview:
```
sed 's/\([A-Za-z0-9_-]*\)\.md/\https\:\/\/html-preview.github.io\/\?url\=https\:\/\/github.com\/MiyooCFW\/docs\/blob\/site-preview\/\1\/index.html/g' mkdocs.yml > mkdocs-preview.yml
python3 -m mkdocs gh-deploy --config-file mkdocs-preview.yml --remote-branch site-preview --no-history
```
