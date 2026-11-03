# Module 6. Geometric PDEs

Notes from the quiz topics of week 6.

- Curves with constant Euclidean curvature: straight lines (zero) and circles. A circle of radius r has
  curvature 1/r.
- The gradient is perpendicular to the level lines of the function.
- div(∇I / |∇I|) is the Euclidean curvature of the level lines.
- Minimizing ∫|∇I|^p: p = 2 gives isotropic diffusion (heat equation), p = 1 gives total variation, which
  diffuses only along edges.
- Curve evolution with level sets: constant normal velocity is f_t = |∇f|; curvature motion is f_t = κ|∇f|.
- Only the normal velocity matters: tangential velocity moves points along the curve but does not change
  its shape.
- Affine arc length: dv = κ^(1/3) ds. For a circle of radius 1/8, κ = 8, so dv = 2 ds.
- To find circular objects of known radius, use the Hough transform rather than a PDE.
