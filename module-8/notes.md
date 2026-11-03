# Module 8. Sparse modeling and compressed sensing

Notes from the quiz topics of week 8.

- A signal is written as x ≈ Dα, with dictionary D (atoms in columns) and few non-zeros in α.
- JPEG uses a fixed dictionary, the DCT. Fixed bases (DCT, Fourier, wavelets) are general but not tuned to
  the data. Learned dictionaries (K-SVD) optimize D and the codes together:
  min ‖α‖₀ subject to Σ ‖Dα_i − y_i‖² ≤ ε.
- A dictionary of random image patches is a fair start, but a learned dictionary of the same size gives
  equal or sparser codes.
- Example: atoms (0,1), (1,1), (0,1), (2,1) and x = (2,2): x = 2·(1,1), so the sparsest code is (0, 2, 0, 0).
- With k atoms and sparsity L there are C(k, L) possible supports (C(100, 3) = 161,700), which is why exact ℓ0
  coding is hard and greedy OMP or ℓ1 relaxation is used. A Gaussian mixture with 100 components has only 100
  subspaces.
- Two complete bases concatenated (e.g. DCT + Fourier) form an overcomplete dictionary; representations are
  not unique, and the sparsity criterion picks one.
- The quadratic data term in sparse denoising comes from assuming Gaussian noise. Other noise models swap the
  data term (e.g. ℓ1 for Laplacian-like noise).
- Sparse modeling is about representing signals; compressed sensing is about acquiring them with far fewer
  measurements, using sparsity to recover them.
- Using patches of the current frame as the dictionary for the next frame gives very sparse codes for a
  static scene, the same redundancy video codecs use.
