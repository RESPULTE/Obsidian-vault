---
type: project
domain: Engineering
status: active
updated: 2026-10-31
---

# Project - Flux Reflow Detection

## Objective

Develop image-based inspection logic to identify suspicious flux/reflow patterns around a die while limiting false positives on acceptable samples. Keep detection decisions explainable and reproducible through debug images and representative tests.

## Localization

- Locate the relevant die or inspection region before analyzing defects.
- Establish the region of interest, boundaries, and any masks used for subsequent detection.
- Record localization assumptions and edge cases separately from the final defect rules.

## Detection Rules

- **Boundary and gap analysis:** Evaluate candidate dark regions near the localized die. Document the current geometric criteria and how gap detection affects classification.
- **Interior voids/bubbles (proposed):** Evaluate enclosed dark regions within the localized area. A proposed validation rule requires a protrusion of at least **3 px** in any direction and an area meeting `AREA_THRESHOLD`; confirm this against the implemented detector and test corpus before treating it as final.
- **Debug visibility:** Show accepted void candidates in red in the relevant debug layer, and trace each decision to its rule.
- **Regression checks:** Include known-good samples and ambiguous cases to monitor false positives and false negatives.

## Lessons Learned

- Separate localization, mask construction, geometric validation, and classification for easier debugging.
- Compare proposed rule changes against the full labeled corpus rather than isolated successes.
- Record the reason for each rule or threshold change together with supporting examples and results.

## Related Concepts

- [[Otsu Thresholding]] — candidate histogram-based thresholding technique for segmentation.
- [[Image Segmentation]] — general foundation for region and mask extraction.
