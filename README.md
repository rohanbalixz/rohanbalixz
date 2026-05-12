<h1 align="center">Rohan Bali</h1>

<p align="center">
  <em>Spatio-temporal machine learning · urban systems · computational social science</em>
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

I build and evaluate machine-learning models for complex spatio-temporal systems — urban growth, elections, collaboration networks — with a focus on what learned representations actually capture, where evaluation metrics fail, and how predictions transfer to regimes they were never trained on.

**M.S. Data Science**, University of Massachusetts Dartmouth · 2024 – 2026
Applying to PhD programs in computer science and societal computing · **Fall 2027 entry**
Boston, MA

---

## Research Interests

`spatio-temporal machine learning` `graph neural networks` `computational social science` `distribution shift & geographic transfer` `evaluation methodology for spatial forecasting` `ML for cities, elections, and public policy`

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
        A controlled isolation experiment across <strong>5,698 CONUS tiles</strong> showing that <strong>94 %</strong> of the apparent architectural advantage of recurrent encoders over convolutional ones at longer urban-growth forecast horizons is a <strong>channel-count confound</strong>, not a property of the architecture. The confound is present in every prior multi-horizon urban-growth benchmark I could identify.
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

- **Channel-matched CNN leads at every horizon.** FoM **0.702 ± 0.019** on the 2015 spatial holdout; **0.252 ± 0.009** on a sealed 2020 temporal holdout.
- **ConvLSTM's multi-horizon gain isolated to a 5.4× asymmetric sensitivity** to terminal-epoch removal — consistent with recency anchoring, not general long-horizon capacity.
- **Algebraic derivation** showing MSE inverts model rankings at growth fractions below ~11 %; FoM is the only operative ranking metric in this regime. Soft-Jaccard (FoM-aligned) training collapses to a near-null predictor — a 4.2× degradation versus MSE training.
- **Zero-shot transfer to Lagos, Nigeria** (20 tiles, 69.6 % growth fraction): recency-anchored ConvLSTM transfers *below* pixel-wise linear extrapolation; flat-channel CNN degrades gracefully.
- **MC Dropout uncertainty calibrated** against empirical error at **r = 0.983** across decile bins; magnitudes underestimated 1.4–1.9×, rank ordering reliable.

#### Venues

- **GeoAI 2026** — 9th ACM SIGSPATIAL International Workshop on Geospatial Artificial Intelligence. Oral presentation. Ghent, Belgium. November 2026.
- **SpatialDI 2026** — 7th International Conference on Spatial Data and Intelligence (ACM SIGSPATIAL China Chapter). Springer LNCS proceedings. Changsha, China. April 2026.

---

## Selected Projects

### Small-World Structure in Academic Collaboration
*Advised by Prof. Dana S. Fine, University of Massachusetts Dartmouth.*

Co-authorship networks constructed and analyzed across **12 academic fields totaling 180K+ edges**. Finding: **72 % of researchers in the top citation percentile sit within a 3-hop neighborhood** of one another in their respective field graphs — with implications for how reputation, ideas, and opportunity propagate through scientific communities.

[Repository →](https://github.com/rohanbalixz/Understanding-Academic-Collaboration-Networks-Through-Small-World-Theory)

### Disaster Risk Monitoring from Satellite Radar
*Completed through the NVIDIA Deep Learning Institute disaster-monitoring track.*

U-Net trained on Sentinel-1 synthetic-aperture-radar imagery for flood-extent detection, with SAR-specific preprocessing (speckle filtering, dB conversion, polarization-aware augmentation). **Dice 0.82 · IoU 0.78.** Inference pipeline integrated with Google Earth Engine.

[Repository →](https://github.com/rohanbalixz/Disaster-Risk-Monitoring-Using-Satellite-Imagery)

---

## Currently

Extending the multi-horizon work toward **causal urban-growth modeling** and characterizing **where predictive models systematically fail across geographies**. Preparing follow-on submissions and PhD applications for Fall 2027.

Open to collaborations in spatio-temporal ML, network science, and computational social systems.

<p align="left">
  <a href="mailto:rohanbaliwork@gmail.com"><img src="https://img.shields.io/badge/Email-rohanbaliwork@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>
