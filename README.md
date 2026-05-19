# lorentz-capacity

This repository contains the source of the technical note
[Spectral Mobility and the Lorentz Factor from Projective Capacity Saturation](out/lorentz-capacity.pdf).

This note establishes that the O7 saturation parameter $\eta_n^{\mathrm{O7}}$, defined
as the ratio of cumulative occupied projective capacity to residual frontier novelty,
converges to the relativistic mobility $\beta\gamma$ in the continuum geometric limit.

## Main Result

Under the Born--Infeld admissibility budget $dI_\tau^2 + dI_{\mathrm{space}}^2 = c_{\mathrm{BI}}^2\,dn^2$
and a quadratic normalization of the O7 observables,

$$\eta_n^{\mathrm{O7}} \longrightarrow \beta\gamma, \qquad
\Phi\!\left(\eta_n^{\mathrm{O7}}\right) = \frac{1}{\sqrt{1+(\eta_n^{\mathrm{O7}})^2}}
\longrightarrow \frac{1}{\gamma}.$$

The inverse Lorentz factor is the residual-capacity profile of the admissible
spectral cascade. The Lorentz factor is not an external kinematical postulate; it
emerges from the occupied-over-residual capacity ratio under a bounded projective budget.

## Structure

The note is organized in five sections:

1. **O7 occupation and residual novelty** — definitions of $B_n$ (cumulative occupation)
   and $\Sigma_n$ (residual frontier novelty) and their ratio $\eta_n^{\mathrm{O7}}$.

2. **Algebraic Born--Infeld target** — purely algebraic derivation showing that
   $\eta = dI_{\mathrm{space}}/dI_\tau$ implies $\Phi(\eta) = 1/\gamma$.

3. **Why the reduced filling model is insufficient** — the linear residual law
   $B_n + \Sigma_n \simeq 1$ does not produce the Lorentzian square root;
   the required structure is the quadratic law $B_n^2 + \Sigma_n^2 \to 1$.

4. **From linear filling to quadratic normalization via Q5b** — the Q5b
   Carnot--Caratheodory continuum limit and Q11 co-metric closure supply the
   geometric upgrade from linear to quadratic normalization.
   The main convergence lemma is stated and identified as the remaining technical task.

5. **Consequence for the Lorentz factor** — Theorem: the O7 profile converges to
   $1/\gamma$, yielding time dilation and the light cone as corollaries.

## Dependencies

- **O7** (`Beau2026a7`): definition of $\eta_n^{\mathrm{O7}}$, $B_n$, $\Sigma_n$,
  and the reduced filling model.
- **Born--Infeld paper** (`Beau2026c`): mobility budget $c_{\mathrm{BI}}$ and
  ordinal cascade depth.
- **Q5b** (`Beau2026q5b`): BFS-to-Carnot--Caratheodory convergence in the
  large-$q$ pre-saturation regime.
- **Q11** (`Beau2026q11`): co-metric closure fixing the Lorentzian signature
  $g^{\mu\nu} = 2\eta^{\mu\nu}$.

## Status

Sections 1--3 and 5 are established. Section 4 contains the open convergence lemma
(Lemma 1) anchored to Q5b/Q11 and left as the remaining technical task.

## Repository Contents

```
lorentz-capacity/
├── out/           # Compiled paper PDF
├── tex/           # LaTeX sources
│   ├── lorentz-capacity.tex
│   └── cosmochrony-bibliography.bib
├── compile.sh     # Compilation script
├── zenodo.json    # Zenodo metadata
└── README.md
```

## Compilation

```bash
bash compile.sh
```

Output: `out/lorentz-capacity.pdf`

## Links

- Paper PDF: [out/lorentz-capacity.pdf](out/lorentz-capacity.pdf)
- Website: [cosmochrony.org](https://cosmochrony.org)

## Citation

> J. Beau, *Spectral Mobility and the Lorentz Factor from Projective Capacity Saturation*, 2026.

## Acknowledgements

Portions of the editorial refinement benefited from iterative interactions with
large language models used as analytical assistants.
All claims, derivations, and interpretations remain the sole responsibility of the author.