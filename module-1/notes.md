# Module 1. Fundamentals

Notes from the quiz topics of week 1.

- Image and video processing shows up in medical imaging, space imaging and consumer photography.
- Images are not limited to the visible spectrum: X-ray, infrared, radio and ultrasound images are processed the same way.
- Brightness adaptation is why you need a moment to see after walking into a dark room.
- Sampling discretizes the spatial domain; quantization discretizes the pixel values.
- Storage = rows × columns × bits per pixel. Fewer gray levels means less memory.
  - 100 × 1000 pixels at 8 bits per pixel = 800,000 bits.
- Video storage = frames per second × seconds × pixels per frame × bits per pixel.
- Pixel adjacency: going from (1,1) to (0,0) takes 1 step with 8-adjacency and 2 steps with 4-adjacency
  (chessboard vs city-block distance).
- A rotation matrix has determinant 1. A scaling matrix has determinant s_x · s_y, so not always 1.
