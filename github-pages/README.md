# GitHub Pages container

Useful to preview a GitHub Pages website locally:

```sh
podman build . -t github-pages
podman run -i --rm -w "$(pwd)" -v "$(pwd):$(pwd):z" --network host github-pages
```
