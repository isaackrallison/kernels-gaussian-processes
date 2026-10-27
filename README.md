# Kernels and GPs Lab

An interactive study guide for §17.1–17.2.2 of Kevin P. Murphy, *Probabilistic Machine Learning: An Introduction*
(Mercer kernels, Mercer's theorem, popular kernels, combining kernels, and Gaussian process regression with noise-free and noisy observations).

**Live:** https://isaackrallison.github.io/kernels-gaussian-processes/

Every section has an **Explain it** box at four levels (Kid, High school, Undergrad, Grad / MLE), switchable globally from the top bar.

- **17.1 Mercer kernels:** drag points on a line and watch the Gram matrix and its eigenvalues update. Try RBF, Matérn ½, linear and polynomial kernels, then two that fail: box similarity and −distance². "Break it" builds the 3-point counterexample. Hunt for c with cᵀKc < 0 (Eqs. 17.1–17.3).
- **17.1.1 Mercer's theorem:** feature vectors φ(xᵢ) = Λ^½ Vᵢ,: read off the Gram matrix above, which fail to exist when λ < 0. The quadratic kernel turns a circle into a straight line (Eq. 17.6). An aside on random Fourier features shows the RBF kernel's infinitely many features.
- **17.1.2.1 Stationary kernels:** K(r) next to three GP samples for SE, Matérn 5/2, 3/2 and ½, periodic, and cosine (Figs 17.2–17.3). The ARD heat map with ℓ₁ and ℓ₂ sliders reproduces Figure 17.1.
- **17.1.2.2–4 New kernels from old:** add or multiply Lin, SE and Per, with presets for Duvenaud's Figures 17.4–17.5. Includes polynomial-kernel feature counts and an n-gram string kernel Gram matrix with a breakdown of shared n-grams.
- **17.2 Gaussian processes:** the joint Gaussian of (f(x₁), f(x*)) as an ellipse, sliced at the observed f(x₁). Figure 17.6 is live, with edge widths set by K.
- **17.2.1 Noise-free observations:** click to condition a GP. Presets for Figure 17.7, posterior samples, a term-by-term table of μ* = k*ᵀα, and cond(K).
- **17.2.2 Noisy observations:** separate sliders for data noise and model σ_y, bands for both f* and y*, Eq. 17.38 drawn as a sum of kernel bumps, an α bar chart, and effective degrees of freedom.
- Step-by-step math for Eqs. 17.1–17.38, a 42-question quiz tagged by level, and a cheat sheet.

Single self-contained `index.html`, no build step. Loads Google Fonts and MathJax from cdnjs. All data are synthetic and generated in the page from fixed seeds.
