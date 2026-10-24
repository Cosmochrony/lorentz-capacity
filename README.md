# lorentz-capacity

This repository contains the source of the technical note
Spectral Mobility and the Lorentz Factor from Projective Capacity Saturation.

The O7 saturation parameter $\eta_n^{\mathrm{O7}}$, the ratio of cumulative occupied projective capacity to
total residual frontier novelty, satisfies the exact linear filling law $B_n + \Sigma_n^{\mathrm{tot}} = 1$
(Weil factorization) and does not by itself yield the Lorentz factor. The note identifies the conditional
mechanism by which a temporally projected residual $\Sigma_n^\tau := \mathcal{P}_\tau^{\mathrm{Q5b}}
\Sigma_n^{\mathrm{tot}}$ does.

## Main Result

Under the quadratic Born-Infeld mobility budget $dI_\tau^2 + dI_{\mathrm{space}}^2 = c_{\mathrm{BI}}^2\,dn^2$,
a hypothesis of the note expressing the capacity bound [A-cap], and the convergence lemma (Lemma 1),

$$\eta_n^\tau := \frac{B_n}{\Sigma_n^\tau} \longrightarrow \beta\gamma, \qquad
\Phi\!\left(\eta_n^\tau\right) = \frac{1}{\sqrt{1+(\eta_n^\tau)^2}}
\longrightarrow \frac{1}{\gamma}.$$

The projection $\mathcal{P}_\tau^{\mathrm{Q5b}}$ is induced by a supplied co-metric of the conditional form of
Q11, $\mathrm{diag}(-A_\tau, 2\lambda, 2\lambda, 2\lambda)$, whose coefficients are independent and fixed by no
source; the normalisation $g^{\mu\nu} = 2\eta^{\mu\nu}$ is a choice of units. Reading $\beta$ as a velocity
relative to the light cone requires the hypothesis **[H-cone]** (light-cone speed equal to the Born-Infeld
bound per ordering step), the coupling datum that Q11 leaves open.

## Structure

The note is organized in five sections:

1. **O7 occupation and residual novelty** — definitions of $B_n$ (cumulative occupation)
   and $\Sigma_n$ (residual frontier novelty) and their ratio $\eta_n^{\mathrm{O7}}$.

2. **Algebraic Born--Infeld target** — purely algebraic derivation showing that
   $\eta = dI_{\mathrm{space}}/dI_\tau$ implies $\Phi(\eta) = 1/\gamma$.

3. **Why the reduced filling model is insufficient** — the linear residual law
   $B_n + \Sigma_n \simeq 1$ does not produce the Lorentzian square root;
   the required structure is the quadratic law $B_n^2 + \Sigma_n^2 \to 1$.

4. **From linear filling to quadratic normalization via Q5b** — the temporal projection
   induced by a supplied co-metric of the conditional form of Q11; the convergence lemma.

5. **Weil factorization** — the central coordinate contributes a global phase, so the linear law
   $B_n + \Sigma_n^{\mathrm{tot}} = 1$ is exact.

6. **Numerical tests** — three candidate observables fail the quadratic law.

7. **Consequence for the Lorentz factor** — conditional theorem: the projected profile converges to
   $1/\gamma$; time dilation and the light cone under [H-cone].

## Dependencies

- **O7** (`Beau2026a11`): definition of $\eta_n^{\mathrm{O7}}$, $B_n$, $\Sigma_n$,
  and the reduced filling model.
- **Born--Infeld paper** (`Beau2026c`): the capacity bound [A-cap] with constant $c_{\mathrm{BI}}$; the
  quadratic budget is a hypothesis of this note.
- **Q5b** (`Beau2026q5b`): BFS-to-Carnot--Caratheodory convergence in the
  large-$q$ pre-saturation regime.
- **Q11** (`Beau2026q11`): conditional rank-four form with two independent coefficients; the temporal
  coefficient and the coupling datum are open.
- **TempProj** (`Beau2026tp`): construction of $\mathcal{P}_\tau^{\mathrm{Q5b}}$ under the hypotheses stated there.

## Status

The Weil factorization and the linear filling law are proved. The Lorentz-factor limit is conditional on
the quadratic budget hypothesis and on the convergence lemma, which TempProj establishes under its own
hypotheses. Its kinematic reading is conditional on [H-cone].

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

- Website: [cosmochrony.org](https://cosmochrony.org)

## Citation

> J. Beau, *Spectral Mobility and the Lorentz Factor from Projective Capacity Saturation*, 2026.

## Acknowledgements

Portions of the editorial refinement benefited from iterative interactions with
large language models used as analytical assistants.
All claims, derivations, and interpretations remain the sole responsibility of the author.