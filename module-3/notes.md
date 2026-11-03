# Module 3. Spatial processing

Notes from the quiz topics of week 3.

- Contrast stretching: I2 = (I1 − m) / (M − m) · L maps [m, M] onto [0, L].
- Histogram equalization:
  - The discrete version does not give a perfectly flat histogram, because all pixels with the same value
    map to the same output value.
  - It is generally not invertible: different input levels can merge.
- N pixels with K levels: K^N images, but only as many histograms as ways to put N pixels into K bins.
  - 2 pixels, 3 values: 9 images, 6 histograms.
- The mean minimizes the sum of squared differences (L2); the median minimizes the sum of absolute
  differences (L1).
- An averaging filter applied infinitely many times converges to the global mean of the image.
- The median filter removes isolated outliers (salt and pepper) and keeps edges; the average smears them.
- Non-local means averages pixels with similar surrounding patches. It is not idempotent and in general
  does not converge to the average.
