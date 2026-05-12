<h1 align="center">Rohan Bali</h1>

<p align="center">
  <em>Geospatial AI · Earth & Climate Systems ML · Spatiotemporal Representation Learning</em>
</p>

<p align="center">
  <a href="https://github.com/rohanbalixz/Multi-Horizon-Urban-Growth-Prediction">
    <img src="https://img.shields.io/badge/GeoAI_2026-Oral-1f6feb?style=flat-square" alt="GeoAI 2026 Oral" />
  </a>
  <a href="https://github.com/rohanbalixz/Multi-Horizon-Urban-Growth-Prediction">
    <img src="https://img.shields.io/badge/SpatialDI_2026-Springer_LNCS-2ea043?style=flat-square" alt="SpatialDI 2026 Springer LNCS" />
  </a>
  <a href="https://scholar.google.com/citations?user=CBgU9IIAAAAJ&hl=en">
    <img src="https://img.shields.io/badge/Google_Scholar-Profile-4285F4?style=flat-square&logo=googlescholar&logoColor=white" alt="Google Scholar" />
  </a>
</p>

<p align="center">
  <a href="https://rohanbalixz.github.io/rohan-bali-portfolio/">Portfolio</a> ·
  <a href="https://scholar.google.com/citations?user=CBgU9IIAAAAJ&hl=en">Scholar</a> ·
  <a href="https://www.linkedin.com/in/rohan-bali-301345293/">LinkedIn</a> ·
  <a href="https://x.com/bali2ro">Twitter / X</a> ·
  <a href="mailto:rohanbaliwork@gmail.com">rohanbaliwork@gmail.com</a>
</p>

---

I build and interrogate machine-learning models for Earth systems — using satellite-derived, 
geophysical, and sociodemographic data to understand how cities grow, landscapes change, 
and climate pressures propagate across space and time.

My research sits at the intersection of spatiotemporal representation learning and 
rigorous evaluation: I care not just about whether a model predicts well, but about 
what its learned representations actually encode, where standard benchmarks silently 
mislead, and whether predictions hold when the geography shifts. Urban growth is my 
proving ground; Earth and climate systems are the destination.

**M.S. Data Science**, University of Massachusetts Dartmouth · 2024 – 2026  
Applying to PhD programs in **Geospatial AI and Earth & Climate Systems ML** · **Fall 2027 entry**  
Boston, MA

---

## Research Interests

`spatiotemporal representation learning` `geospatial AI` `earth observation & remote sensing`
`climate & land systems ML` `distribution shift & geographic transfer` 
`benchmark design & evaluation methodology` `uncertainty quantification`

---

## Featured Publication

<table>
  <tr>
    <td width="42%" valign="top">
      <img src="https://github.com/rohanbalixz/Multi-Horizon-Urban-Growth-Prediction/blob/main/results/figures/fig7_uncertainty.png" alt="Mid-Atlantic held-out tile: ground truth, ConvLSTM prediction, and MC Dropout uncertainty" />
      <p align="center"><sub><em>Mid-Atlantic held-out tile — ground truth, ConvLSTM prediction, and MC Dropout uncertainty (20 stochastic forward passes).</em></sub></p>
    </td>
    <td width="58%" valign="top">
      <h3>Channel Count, Not Horizon Length, Drives Architectural Divergence in Multi-Horizon Urban Growth Prediction</h3>
      <p><strong>Rohan Bali.</strong> Solo-authored.</p>
      <p>
        <img src="https://img.shields.io/badge/GeoAI_2026-Oral-1f6feb?style=flat-square" alt="GeoAI 2026 Oral" />
        <img src="https://img.shields.io/badge/SpatialDI_2026-Springer_LNCS-2ea043?style=flat-square" alt="SpatialDI 2026 Springer LNCS" />
      </p>
      <p>
        A controlled isolation experiment across <strong>5,698 CONUS tiles at 250 m</strong> 
        showing that <strong>94%</strong> of the apparent architectural advantage of recurrent 
        encoders over convolutional ones at longer forecast horizons is a 
        <strong>channel-count confound</strong> — present in every prior multi-horizon 
        urban-growth benchmark examined. Urban growth as testbed; the findings apply 
        wherever multi-horizon benchmarks shorten the encoder window as the prediction 
        target moves forward.
      </p>
      <p>
        <a href="https://github.com/rohanbalixz/Multi-Horizon-Urban-Growth-Prediction"><strong>Code & data</strong></a> ·
        <a href="https://github.com/rohanbalixz/NeuralTimeCapsule"><strong>NeuralTimeCapsule repo</strong></a> ·
        <em>arXiv pending</em>
      </p>
    </td>
  </tr>
</table>

#### Key results

- **Channel-matched CNN leads at every horizon.** FoM **0.702 ± 0.019** on the 2015 spatial holdout; **0.252 ± 0.009** on a fully sealed 2020 temporal holdout — trained weights never touched 2020 data.
- **ConvLSTM's multi-horizon gain traced to a 5.4× asymmetric sensitivity** to terminal-epoch removal — recency anchoring in the hidden state, not general long-horizon architectural capacity.
- **Algebraic derivation** showing MSE inverts model rankings at growth fractions below ~11%; FoM is the only operative metric in this regime. FoM-aligned Soft-Jaccard training collapses to a near-null predictor — a 4.2× degradation versus MSE training evaluated under FoM.
- **Zero-shot transfer to Lagos, Nigeria** (20 tiles, 69.6% growth fraction): recency-anchored ConvLSTM transfers *below* pixel-wise linear extrapolation; flat-channel CNN degrades gracefully — consistent with domain-specific hidden-state encoding as the failure mechanism.
- **MC Dropout uncertainty calibrated** at **r = 0.983** across decile bins (≈8.7M pixels); rank ordering reliable for field prioritization; magnitudes underestimated 1.4–1.9× without post-hoc scaling.

#### Venues

- **GeoAI 2026** — 9th ACM SIGSPATIAL International Workshop on Geospatial Artificial Intelligence. Oral presentation. Ghent, Belgium. November 2026.
- **SpatialDI 2026** — 7th International Conference on Spatial Data and Intelligence (ACM SIGSPATIAL China Chapter). Springer LNCS proceedings. Changsha, China. April 2026.

---

## Selected Projects

### Disaster Risk Monitoring from Satellite Radar
*NVIDIA Deep Learning Institute · Earth Observation Track*

U-Net trained on Sentinel-1 synthetic-aperture-radar imagery for flood-extent detection 
at scale, with SAR-specific preprocessing (speckle filtering, dB conversion, 
polarization-aware augmentation). **Dice 0.82 · IoU 0.78.** Inference pipeline 
integrated with Google Earth Engine for operational deployment.

This project and the urban growth work share a common thread: both use multitemporal 
satellite observation stacks to detect where and how Earth's surface is changing — 
and both expose where standard ML pipelines silently fail on geospatial data.

[Repository →](https://github.com/rohanbalixz/Disaster-Risk-Monitoring-Using-Satellite-Imagery)

### Small-World Structure in Academic Collaboration
*Advised by Prof. Dana S. Fine, University of Massachusetts Dartmouth*

Co-authorship networks constructed and analyzed across **12 academic fields, 180K+ edges**. 
Finding: **72% of researchers in the top citation percentile sit within a 3-hop neighborhood** 
of one another — with implications for how ideas, reputation, and opportunity concentrate 
and propagate through scientific communities.

[Repository →](https://github.com/rohanbalixz/Understanding-Academic-Collaboration-Networks-Through-Small-World-Theory)

---

## Currently

Extending the multi-horizon work toward **causal land-cover and climate-system modeling** — 
asking not just where growth or change will occur, but what drives it, and whether 
those drivers transfer across geographies and climate regimes. Preparing follow-on 
submissions and PhD applications for Fall 2027.

Open to collaborations in geospatial AI, earth observation ML, and spatiotemporal 
representation learning.

<p align="left">
  <a href="mailto:rohanbaliwork@gmail.com">
    <img src="https://img.shields.io/badge/Email-rohanbaliwork@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>
