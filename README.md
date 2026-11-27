# GENUS · data

Large data files of [GENUS](https://github.com/genus-collab) projects: files too large to keep in the
thematic repositories (above about 20 MB each, or large sets of machine-generated files).

**The files themselves are release assets, not part of the git history.** This keeps every clone small.
The repository holds one folder per project, with a README (what each file is, its conventions, how it
was computed) and a `SHA256SUMS` list.

| Project | Folder | Release |
|---|---|---|
| solutions/resolved-conifold-cy-torus | [`projects/solutions/resolved-conifold-cy-torus`](projects/solutions/resolved-conifold-cy-torus/) | [`solutions/resolved-conifold-cy-torus/v1`](https://github.com/genus-collab/data/releases/tag/solutions/resolved-conifold-cy-torus/v1) |
| solutions/refined-gap-local-p2 | [`projects/solutions/refined-gap-local-p2`](projects/solutions/refined-gap-local-p2/) | [`solutions/refined-gap-local-p2/v1`](https://github.com/genus-collab/data/releases/tag/solutions/refined-gap-local-p2/v1) |
| solutions/conifold-gap-formal-quintic | [`projects/solutions/conifold-gap-formal-quintic`](projects/solutions/conifold-gap-formal-quintic/) | [`solutions/conifold-gap-formal-quintic/v1`](https://github.com/genus-collab/data/releases/tag/solutions/conifold-gap-formal-quintic/v1) |

## Layout

- `projects/<strand>/<project>/README.md`: description of the data and link back to the project.
- `projects/<strand>/<project>/SHA256SUMS`: checksums of the release assets and of the files inside them.
- Release tag `<strand>/<project>/v<n>`: the assets. A new version gets a new release; old releases are never deleted.

## Downloading

```
gh release download <strand>/<project>/v<n> -R genus-collab/data -D <folder>
cd <folder> && sha256sum -c SHA256SUMS
```

Without the GitHub CLI, the assets can be downloaded from the release page.

## Adding data

Open a PR here adding the project's folder (README and `SHA256SUMS`), and ask a maintainer to create the
release with the assets. The project's own `data/README.md` links here. Data should be plain text
(compressed archives of plain-text files are fine).

## Licence

Data: CC0 1.0 Universal (see [`LICENSE`](LICENSE)). READMEs: CC BY 4.0, attribution to "the GENUS collaboration".
