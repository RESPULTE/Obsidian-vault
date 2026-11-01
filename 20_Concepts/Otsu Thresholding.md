---
type: concept
domain: Computer Vision
parent: "[[Image Segmentation]]"
aliases: [Otsu's Method, Global Binarization, Histogram Thresholding]
status: active
updated: 2026-10-31
---

# Otsu Thresholding

## Summary

**Otsu thresholding** is an automatic, global image-binarization method that selects a grayscale threshold from an image's intensity histogram. It is useful when foreground and background intensities form reasonably distinct groups.

## Core Mechanism

1. Compute the grayscale histogram.
2. For each candidate threshold, split pixels into two intensity classes.
3. Select the threshold that **maximizes between-class variance** (equivalently, minimizes weighted within-class variance).
4. Binarize the image into foreground and background using that threshold.

**Limitation:** One global threshold can perform poorly with uneven illumination, substantial noise, or overlapping foreground/background intensities.

## Related Concepts & Applications

- [[Image Segmentation]] — broader task of separating meaningful regions in an image.
- [[Project - Flux Reflow Detection]] — a potential segmentation technique to evaluate for extracting dark regions; suitability must be verified against actual inspection samples.
