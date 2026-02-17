# Unit 01 - Week 04 (Image Features and Classical Feature Extractors)

## 1) What Are Image Features?
- Features are distinctive image patterns (edges, corners, blobs, textures).
- They act like landmarks for tasks such as matching, tracking, and recognition.

## 2) Local vs Global Features
- **Global features:** summarize the whole image (overall texture/color/statistics).
- **Local features:** computed around keypoints; useful for matching objects across views.

## 3) Good Feature Properties
A good feature should be:
- **Invariant** (to scale/rotation/illumination/view changes)
- **Repeatable** (re-detected under similar conditions)
- **Distinctive** (easy to match uniquely)

## 4) Feature Extraction
- Converts raw pixels into compact, meaningful descriptors.
- Reduces complexity and supports higher-level CV tasks.

## 5) SIFT (Scale-Invariant Feature Transform)
- Robust detector + descriptor.
- Main pipeline:
  1. Scale-space extrema detection (DoG)
  2. Keypoint localization/refinement
  3. Orientation assignment
  4. Descriptor generation (typically 128-D)
- Strong for scale and rotation changes.

## 6) FAST Corner Detector
- Very fast corner detector for real-time use.
- Uses intensity comparisons on a 16-pixel circle around a candidate point.
- Usually followed by non-maximum suppression.
- FAST detects keypoints only (not descriptors).

## 7) SURF (Speeded Up Robust Features)
- Inspired by SIFT, designed to be faster.
- Uses integral images + box filters + Hessian-based detection.
- Provides both keypoints and descriptors.

## 8) BRIEF Descriptor
- Binary descriptor based on simple intensity pair comparisons.
- Very fast and compact.
- Limitation: not inherently scale/rotation invariant.

## 9) ORB (Oriented FAST and Rotated BRIEF)
- Combines FAST keypoints with rotated BRIEF descriptors.
- Fast, robust, patent-free, and practical for real-time/commercial use.

## 10) Key Takeaway
- Feature extraction quality strongly affects downstream vision tasks.
- No single extractor is best for every case; choose based on speed, robustness, and application constraints.
