# solutions / conifold-gap-formal-quintic

Large files of the GENUS project
[solutions/projects/conifold-gap-formal-quintic](https://github.com/genus-collab/solutions/tree/main/projects/conifold-gap-formal-quintic)
(conifold regularity of the formal quintic, graph by graph). Release:
[`solutions/conifold-gap-formal-quintic/v1`](https://github.com/genus-collab/data/releases/tag/solutions/conifold-gap-formal-quintic/v1).

| Asset | Size | Contents |
|---|---|---|
| `g5_evidence.tar.gz` | 46 MB (113 MB unpacked, 1061 entries) | `logs/` and `parts/` of the five genus-5 cluster runs on Stanage (point frame and natural frame, modulo 2^89 − 1 and 2^61 − 1): the per-task logs and the partial results per outer graph, as copied back from the cluster. Read by the audit scripts in `hodge_vertex_quintic/natural_form/genus5_cluster/` (`indep/`, `census/`), which look for it in `g5ev/` at the top of `code/` (environment variable `G5EV` to override) |
| `parts_g5_89_nat_local.json.gz` | 8.5 MB (23 MB unpacked) | `hodge_vertex_quintic/natural_form/genus5_cluster/local/out/parts_g5_89_nat_local.json`: partial results of the local rerun of the genus-5 natural-frame computation modulo 2^89 − 1, made for the audit of the cluster evidence |

Both are plain text (logs and JSON), compressed. Unpack into `code/` of the project:

```
gh release download solutions/conifold-gap-formal-quintic/v1 -R genus-collab/data -D dl
cd dl && sha256sum -c <path>/SHA256SUMS
mkdir -p <project>/code/g5ev && tar xzf g5_evidence.tar.gz -C <project>/code/g5ev
mkdir -p <project>/code/hodge_vertex_quintic/natural_form/genus5_cluster/local/out
gunzip -c parts_g5_89_nat_local.json.gz > <project>/code/hodge_vertex_quintic/natural_form/genus5_cluster/local/out/parts_g5_89_nat_local.json
cd <project>/code && sha256sum -c <path>/SHA256SUMS.contents
```

Licence: CC0 1.0 (data). Credited to the GENUS collaboration.
