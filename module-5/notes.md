# Module 5. Image segmentation

Notes from the quiz topics of week 5.

- Otsu's method computes the threshold automatically by maximizing the between-class variance. That is the
  difference from simple thresholding.
  - The threshold is not necessarily unique (any value in an empty gap of the histogram is equally good).
  - Multimodal histograms: multi-level Otsu (several thresholds) or Otsu applied recursively.
- Mumford–Shah penalizes both the misfit to piecewise-constant regions and the total boundary length.
  Combined with Otsu: add a length term to the criterion and search for the best threshold.
- Graph cuts: edge weights between neighbouring pixels are a function of their gray/color difference.
- Hough transform: detects parametric shapes by voting in parameter space.
  - Line: 2 parameters. Circle: 3. Ellipse: 5.
  - Works for any shape with a parametric form.
