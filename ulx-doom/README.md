# ulx-doom

This is the source code directory for the Hazard3 [ulx3s.github.io/ulx-doom](https://ulx3s.github.io/ulx-doom/) quick start instructions.

The local, lower-case [../hazard3-doom](../hazard3-doom/README.md) is a just redirect to [ulx3s.github.io/Hazard3-Doom](https://ulx3s.github.io/Hazard3-Doom),
which is published with GH pages from `ulx3s/Hazard3-Doom`. See [github.com/ulx3s/Hazard3-Doom/settings/pages](https://github.com/ulx3s/Hazard3-Doom/settings/pages).

The entire `Hazard3-Doom` repo is NOT a GH Page site. See the [publishing workflow](https://github.com/ulx3s/Hazard3-Doom/blob/main/.github/workflows/pages.yml) `pages.yml`:

Only the `with:` setting for the [web](https://github.com/ulx3s/Hazard3-Doom/tree/main/web) subdirectory in `path:` is published:

```yaml
        steps:
            - name: Checkout
              uses: actions/checkout@v6

            - name: Configure Pages
              uses: actions/configure-pages@v6

            - name: Upload web UI
              uses: actions/upload-pages-artifact@v5
              with:
                  path: web   # <<<<<< only the web subdirectory is published as https://ulx3s.github.io/Hazard3-Doom/  <<<

            - name: Deploy
              id: deployment
              uses: actions/deploy-pages@v5
```
