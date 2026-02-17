# Unit 01 - Week 01 (Traditional Computer Vision)

## 1) What is an Image?
- An image is a visual representation of a person, object, or scene.
- It can be captured by cameras/scanners/satellites or created digitally.

## 2) Analog vs Digital Images
- **Analog image:** continuous representation (film, paintings, printed photos), not pixel-based.
- **Digital image:** made of pixels and stored as a matrix (rows × columns).
- Common image types:
  - **Binary:** black/white only
  - **Grayscale:** shades of gray
  - **RGB color:** red, green, blue channels

## 3) Image Size and Representation
- **Dimensions:** width × height (pixels)
- **Bit depth:** bits per pixel (controls color/intensity range)
- **File size:** depends on resolution and format (JPEG, PNG, etc.)
- Computers represent images as:
  - 2D array for grayscale
  - 3D array for color (H × W × 3)

## 4) Image as a Function
- Grayscale image: **f(x, y)**
- Color image: **f(x, y, c)** where c ∈ {R, G, B}
- Since an image is a function, operations like add/subtract can be applied.
- Subtraction is useful for change/motion detection.

## 5) 3D to 2D Projection Basics
- Perspective projection maps 3D world points onto a 2D image plane.
- Farther objects appear smaller because depth affects projected size.
- Key model: **pinhole camera model**.
- Orthographic projection keeps scale constant (no perspective distortion).

## 6) Camera Models
- **Pinhole camera:** simplest model, forms an inverted image through a tiny aperture.
- **Analogue camera:** uses lens + film (chemical light response).
- **Digital camera:** uses lens + image sensor made of pixels.

## 7) Camera Calibration Concepts
- **Extrinsics:** camera position/orientation relative to world coordinates.
- **Intrinsics:** focal lengths, optical center, and other internal camera parameters.
- Calibration helps convert 3D world coordinates into 2D image/pixel coordinates.

## 8) Coordinate Conversion Pipeline
Typical mapping steps:
1. World coordinates
2. Camera coordinates
3. Image coordinates
4. Pixel coordinates

Often written with matrices (intrinsic **K**, rotation **R**, translation **T**).

## 9) Assignment (from slides)
- Build a physical pinhole camera model.
- List and explain common image formats (JPEG/JPG, PNG, GIF, BMP, TIFF/TIF, WEBP, HEIF/HEIC, PGM, SVG, AI, EPS, PDF).

## 10) Quick Summary
- Images are mathematical objects and can be processed systematically.
- Perspective projection and camera models are foundational.
- Intrinsic/extrinsic parameters are essential for 3D understanding.
