# solutions / resolved-conifold-cy-torus

Large files of the GENUS project
[solutions/projects/resolved-conifold-cy-torus](https://github.com/genus-collab/solutions/tree/main/projects/resolved-conifold-cy-torus)
(refined GW theory of the resolved conifold × C² on the Calabi–Yau torus). Release:
[`solutions/resolved-conifold-cy-torus/v1`](https://github.com/genus-collab/data/releases/tag/solutions/resolved-conifold-cy-torus/v1).

| Asset | Size | Contents |
|---|---|---|
| `hvc_terms_g4_Bm.tar.gz` | 63 MB (230 MB unpacked) | the 120 chunk files `stanage_genus4/hvc_terms_g4_Bm_c<k>of120.m` of the genus-4 Hodge-vertex graph sum, frame B, h_w^{-1} (Stanage run of 2026-10-30): one entry per decorated graph (27172 in all): id {stable graph, orbit}, key {psi powers on half-edges, dilaton leaves}, description, term (exact rational function of Q and x = ε₁/ε₂), polar part at Q = 1 {t^-6, …, t^-1}, symmetry flag. Written by `hvc_run.wls orbits 4 B m <k> 120`; read by `hvc_run.wls collect 4 B m` |
| `engine_h5_r7.txt.gz` | 11 MB (75 MB unpacked) | `lemmaA/E_formulas/engine_h5_r7.txt`: component polynomials of the Lemma A engine at h = 5, r = 7 (2 016 585 coefficients), compared coefficient by coefficient by the referee of `lemmaA/E_formulas/referee.md` |

Both are plain text (Mathematica `InputForm` and plain tables), compressed. Unpack them into
`code/hodge_vertex_conifold/` of the project:

```
gh release download solutions/resolved-conifold-cy-torus/v1 -R genus-collab/data -D dl
cd dl && sha256sum -c ../projects/solutions/resolved-conifold-cy-torus/SHA256SUMS   # or copy SHA256SUMS here first
tar xzf hvc_terms_g4_Bm.tar.gz -C <project>/code/hodge_vertex_conifold
gunzip -c engine_h5_r7.txt.gz > <project>/code/hodge_vertex_conifold/lemmaA/E_formulas/engine_h5_r7.txt
cd <project>/code/hodge_vertex_conifold && sha256sum -c <path>/SHA256SUMS.contents
```

`SHA256SUMS` lists the assets; `SHA256SUMS.contents` lists the 121 files inside them.

Licence: CC0 1.0 (data). Credited to the GENUS collaboration.
