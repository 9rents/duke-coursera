# Module 2. Image compression

Notes from the quiz topics of week 2.

- Variable-length coding gains nothing when all gray levels are equally likely: the entropy is already maximal.
- Predictive coding makes lossless compression effective by coding the prediction error, whose histogram
  is sharply peaked, instead of the raw pixels.
- The prediction can only use pixels that are already decoded, not any pixel in the image.
- Huffman codes are not unique. Swapping 0/1 or breaking ties differently gives other valid codes with the
  same average length.
  - Probabilities 3/8, 1/8, 1/8, 3/8 can give code lengths 1, 3, 3, 2.
- JPEG:
  - 8×8 blocks → DCT → quantization → entropy coding.
  - Quantization is the only significant source of loss.
  - The DCT is preferred over the Fourier transform because it is real-valued and compacts energy better.
  - A larger quantization step gives a higher compression ratio, but not proportionally.
  - JPEG can go far below 1 bit per pixel, so the ratio is not capped at 8:1.
