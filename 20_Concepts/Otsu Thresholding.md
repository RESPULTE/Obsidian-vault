---
type: concept
domain: Computer Vision
parent: "[[Image Segmentation]]"
aliases: [Otsu's Method, Global Binarization, Histogram Thresholding]
status: active
updated: 2026-11-01
---

# Otsu Thresholding

**Summary:** **Otsu thresholding** is an automatic, global image-binarization method that selects a grayscale threshold from an image's intensity histogram. It is useful when foreground and background intensities form reasonably distinct groups.

## Core Mechanism / Theory

1. Compute the grayscale histogram.
2. For each candidate threshold, split pixels into two intensity classes.
3. Select the threshold that **maximizes between-class variance** (equivalently, minimizes weighted within-class variance).
4. Binarize the image into foreground and background using that threshold.

## Trade-offs & Limitations

- One global threshold can perform poorly with uneven illumination, substantial noise, or overlapping foreground/background intensities.
- Otsu does not mathematically require a perfectly bimodal histogram, but separable intensity groups generally make its threshold more useful. Extra bright reflections can change the class distributions and cause misclassification when a single threshold no longer separates the intended regions.
- [[Specular Glare in Image Thresholding]] describes this illumination-related failure mode. A ring-light/PCB solder-paste example was captured, but no images or measurements were provided to verify failure in that specific setup; see [[2026-11-01 - Ring-Light Glare and Otsu Thresholding]].

## Related Concepts & Applications

- [[Image Segmentation]] — broader task of separating meaningful regions in an image.
- [[Specular Glare in Image Thresholding]] — effect of specular highlights on intensity-based segmentation.
- [[Project - Flux Reflow Detection]] — a potential segmentation technique to evaluate for extracting dark regions; suitability must be verified against actual inspection samples, and the solder-paste glare example has not been linked to this project.
