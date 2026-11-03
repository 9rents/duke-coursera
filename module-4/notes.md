# Module 4. Image restoration

Notes from the quiz topics of week 4.

- Uniform noise on [a, b] has variance (b − a)² / 12.
- Gaussian noise gives a Gaussian mode in the histogram of a flat region.
- Salt-and-pepper noise: p(z) = Pa at z = a, Pb at z = b, 0 otherwise.
- Enhancement improves appearance; restoration tries to recover the original using a model of the degradation.
- The Wiener filter minimizes the expected mean squared error for blur plus noise. The plain inverse filter
  divides by near-zero frequencies and amplifies noise.
- The prediction error of a piecewise-constant image is zero except at edges. With added Gaussian noise it
  becomes several Gaussian modes: one around zero and one at each edge jump.
