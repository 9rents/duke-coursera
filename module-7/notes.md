# Module 7. Image and video inpainting

Notes from the quiz topics of week 7.

- PDE-based inpainting propagates some quantity L into the hole along a direction N: ∇L · N = 0.
  - With N = (∇I)^⊥ (along the isophotes), propagating I itself is useless: ∇I · (∇I)^⊥ = 0 for any image,
    so every fill satisfies it.
  - Propagating the Laplacian of I carries smoothness into the hole and gives a meaningful continuation.
- Variational inpainting minimizes an energy (data term plus regularity of the level lines) instead.
- Smart cut-and-paste (exemplar-based) copies the best-matching patch from elsewhere in the image. It
  reproduces texture, which PDEs cannot. Filling one pixel per match costs about N × M patch comparisons
  (N missing pixels, M pixels in the image).
- Choosing a method:
  | Situation | What works |
  |---|---|
  | Part of a known shape (e.g. a circle) is covered | detect it globally (Hough) and redraw it |
  | Thin 1-pixel scratches in flat areas | simple linear interpolation |
  | Large textured holes | exemplar-based / texture synthesis |
  | Structure and texture together | combine PDE and exemplar methods |
- Video: to remove a fast-moving object, take the temporal median over (x, y, t). The object is an outlier at
  each pixel; a temporal average would leave a ghost.
- Vertical scratches in old film: detect the lines with the Hough transform, then interpolate if they are thin.
