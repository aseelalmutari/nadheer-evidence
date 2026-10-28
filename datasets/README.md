# Dataset Sources

This page documents source provenance and project use. It does not redistribute third-party audio. Licence and attribution notes below reflect the source pages as consulted by the author; readers should consult the original sources.

| Dataset | Original source | Role in NADHEER | Recorded license information | Attribution/licence note |
|---|---|---|---|---|
| UaVirBASE | [Zenodo record 15391924](https://zenodo.org/records/15391924) | Multichannel real-drone recordings; normalized derivatives contributed to drone data and later frozen validation provenance | The live Zenodo record metadata states CC BY 4.0. | Cite the dataset article and Zenodo record shown below. |
| DroneNoise Database | [University of Salford Figshare](https://salford.figshare.com/articles/dataset/DroneNoise_Database/22133411) | Real-drone audio used after resampling | The live Figshare source page states CC BY 4.0. | Cite version 3 of the Figshare dataset shown below. |
| Drone Audio Detection Samples (DADS) | [Hugging Face dataset card](https://huggingface.co/datasets/geronimobasso/drone-audio-detection-samples) | Drone and non-drone samples used in the binary dataset | The live dataset page labels DADS as MIT; its licensing section says source data use various Creative Commons Attribution and similar open licenses and directs users to verify each source for commercial and non-commercial use. | Cite the dataset card; upstream-source terms remain relevant to source recordings. |
| ESC-50 | [Official repository](https://github.com/karolpiczak/ESC-50) and [per-clip LICENSE file](https://github.com/karolpiczak/ESC-50/blob/master/LICENSE) | Environmental confusers used to harden the binary classifier | The repository states that ESC-50 as a whole is CC BY-NC and the ESC-10 subset is CC BY. Its LICENSE file records the underlying Freesound attribution/license for each clip, including CC0, CC-BY, CC-BY-NC, and CC-Sampling+. This package redistributes no ESC-50 or other third-party audio. | Cite the dataset paper and repository; the per-clip LICENSE file records source-specific attribution. |

## Attribution

1. G. Jekateryńczuk, R. Szadkowski, and Z. Piotrowski, “UaVirBASE: A Public-Access Unmanned Aerial Vehicle Sound Source Localization Dataset,” *Applied Sciences*, vol. 15, no. 10, article 5378, 2025. https://doi.org/10.3390/app15105378. Dataset record: https://doi.org/10.5281/zenodo.15391924. License recorded by Zenodo: CC BY 4.0.
2. C. Ramos-Romero, A. J. Torija Martinez, N. Green, and C. Asensio, *DroneNoise Database*, version 3, University of Salford Figshare, 2024. https://doi.org/10.17866/rd.salford.22133411. License recorded by Figshare: CC BY 4.0.
3. G. Basso, *Drone Audio Detection Samples (DADS)*, Hugging Face Datasets, n.d. https://huggingface.co/datasets/geronimobasso/drone-audio-detection-samples. The dataset page labels the dataset MIT and directs users to verify the licences of its upstream audio sources.
4. K. J. Piczak, “ESC: Dataset for Environmental Sound Classification,” in *Proceedings of the 23rd ACM International Conference on Multimedia*, 2015, pp. 1015–1018. https://doi.org/10.1145/2733373.2806390. The repository states CC BY-NC for ESC-50 and CC BY for ESC-10; per-clip source licences and attribution are recorded in the repository LICENSE file.

## Boundaries

- Dataset links and aggregate counts do not imply ownership of the underlying recordings.
- No raw or derived third-party audio belongs in the public evidence package without a documented redistribution review.
- This repository redistributes no third-party audio.
- Internal evaluation on these sources is not field performance.
