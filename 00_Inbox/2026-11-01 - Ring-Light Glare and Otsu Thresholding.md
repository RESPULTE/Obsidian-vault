---
type: finding
domain: Computer Vision
parent: "[[Otsu Thresholding]]"
aliases: [Ring-Light Specular Glare, Otsu Glare Failure, PCB Solder Paste Thresholding]
status: unprocessed
updated: 2026-11-01
---

# Ring-Light Glare and Otsu Thresholding

## Raw finding

Specular glare from ring-light LEDs reflecting off PCB solder paste causes Otsu thresholding to fail because it skews the expected bimodal grayscale-intensity histogram.

## Mechanism discussed

- Ring-light illumination produces bright specular reflections on the solder-paste surface.
- These highlights distort the intensity distribution, so the histogram no longer represents a clean separation between the intended foreground and background classes.
- Otsu's globally selected threshold can therefore misclassify pixels and produce unreliable binarization of the solder-paste region.

## Source and context

Captured from discussion on 2026-11-01. This is the discussed observation; no example images, histogram plots, or measurements were provided in the capture.

Related vault concept: [[Otsu Thresholding]].
Existing project referencing Otsu: [[Project - Flux Reflow Detection]] (relationship of this specific PCB solder-paste glare case to the project remains to be verified during inbox processing).
