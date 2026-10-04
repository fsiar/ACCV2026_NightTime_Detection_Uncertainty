# On the Uncertainty of Night-Time Traffic Object Detection: Annotation or Enhancement, What Matters More?

**ACCV 2026 — 18th Asian Conference on Computer Vision**  
**Authors:** Fatemeh Siar and Francisco C. Pereira

> Official companion repository for our ACCV 2026 paper on annotation, image enhancement, and uncertainty in night-time road-object detection.

**Keywords:** Night-Time Object Detection · Low-Light Vision · Image Enhancement · Traffic Scenes · Evidential Deep Learning · Uncertainty Quantification

## Overview

Night-time traffic object detection is challenging because illumination is non-uniform, noise is substantial, and important road users or small objects can be difficult to distinguish. This work investigates what contributes more to reliable detection: enhancing images, or including annotated dark data in detector training. It also examines prediction reliability under difficult lighting conditions.

We construct a dataset of **13,127 annotated frames**, involving **more than 800 hours of manual annotation**, and follow an **annotate-once, use-twice** workflow: labels created with the assistance of enhanced frames are transferred to the corresponding original dark frames.

We compare four YOLOv8x training configurations:

| Configuration | Training data |
|:--|:--|
| **V1** | Light |
| **V2** | Light + Dark |
| **V3** | Light + Dark + Enhanced |
| **V4** | Light + Enhanced |

Our experiments show that **annotated raw dark images provide a stronger standalone training signal than enhanced night images**, while training with both dark and enhanced images provides the strongest overall results in the primary YOLOv8x comparison. We further study a lightweight evidential reliability head for prediction-level trust and representation support.

## Materials

This repository accompanies the paper. Extended material may be added progressively, including:

- Supplementary analyses, statistical results, and per-class evaluations.
- Qualitative comparisons and additional visualizations.
- Code and experimental configurations.
- Model weights for V1–V4 and uncertainty analysis resources.
- Dataset annotation and split specifications, where redistribution is permitted.

Please check the repository contents for currently available files; listing an item here does not mean it has already been released.

## Dataset and privacy

The research involves traffic-video data from Denmark, Germany, and Myanmar. Due to data-protection, privacy, and third-party rights considerations, **the original traffic recordings and annotated traffic images are not automatically available for public redistribution**. Any released annotations, crops, configurations, or other materials will be accompanied by their applicable usage conditions.

## Citation

**If you use this work or any part of the repository—including the dataset, annotations, code, model weights, figures, supplementary material, or experimental results—in your research, please cite our paper:**

> Fatemeh Siar and Francisco C. Pereira.  
> *On the Uncertainty of Night-Time Traffic Object Detection: Annotation or Enhancement, What Matters More?*  
> Asian Conference on Computer Vision (ACCV), 2026.

The official proceedings BibTeX entry and paper link will be added when available.

## License

Original code explicitly released under the repository's [MIT License](LICENSE) may be reused under its terms. Dataset materials, annotations, figures, third-party assets, model weights, and restricted footage may have separate terms; check the accompanying notices before reuse. We also request citation of the associated ACCV 2026 paper in academic work.
