# solutions / refined-gap-local-p2

Large files of the GENUS project
[solutions/projects/refined-gap-local-p2](https://github.com/genus-collab/solutions/tree/main/projects/refined-gap-local-p2)
(refined conifold gap and regularity of stable graphs for local P² × C²). Release:
[`solutions/refined-gap-local-p2/v1`](https://github.com/genus-collab/data/releases/tag/solutions/refined-gap-local-p2/v1).

| Asset | Size | Contents |
|---|---|---|
| `hv_terms_g4.tar.gz` | 4.6 MB (36 MB unpacked) | the 120 chunk files `hodge_vertex/stanage_run_2026-10-30/hv_terms_g4_c<k>of120.m` of the genus-4 Hodge-vertex graph sum (Stanage run of 2026-10-30): the term of every decorated graph (27172 in all), as reconstructed on the cluster |
| `hodge_graphterms_genus4.m.gz` | 3.5 MB (36 MB unpacked) | `hodge_vertex/hodge_graphterms_genus4.m`: the assembled genus-4 terms, one entry per decorated graph with key, description, term and conifold polar part; read by the genus-4 section of `hodge_vertex/localp2CY5_hodge_genus3.nb` |
| `StableGraph-7.bin.gz` | 4.0 MB (72 MB unpacked) | `StableGraph-7.bin`: the genus-7 stable graphs in the binary format of `StableGraph-2..6.bin` (read by `graphs.m`); not used by the stored computations, which stop at genus 4 |

The `.m` files are plain text (Mathematica `InputForm`), compressed. Unpack into `code/` of the project:

```
gh release download solutions/refined-gap-local-p2/v1 -R genus-collab/data -D dl
cd dl && sha256sum -c <path>/SHA256SUMS
tar xzf hv_terms_g4.tar.gz -C <project>/code
gunzip -c hodge_graphterms_genus4.m.gz > <project>/code/hodge_vertex/hodge_graphterms_genus4.m
gunzip -c StableGraph-7.bin.gz > <project>/code/StableGraph-7.bin
cd <project>/code && sha256sum -c <path>/SHA256SUMS.contents
```

`SHA256SUMS` lists the assets; `SHA256SUMS.contents` lists the 122 files inside them.

Licence: CC0 1.0 (data). Credited to the GENUS collaboration.
