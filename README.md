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

I work on ML for spatiotemporal systems, mostly using satellite and geophysical data.
The questions I keep coming back to: what does a model actually learn from a sequence
of observations, when does that break down, and does it still hold somewhere it was
never trained?

Urban growth is where I've been working. Earth and climate systems are where I'm headed.

**M.S. Data Science**, University of Massachusetts Dartmouth · 2024 – 2026  
Applying to PhD programs in Geospatial AI and Earth & Climate Systems ML · Fall 2027  
Boston, MA

---

## Research Interests

`spatiotemporal representation learning` `geospatial AI` `earth observation & remote sensing`
`climate & land systems ML` `distribution shift & geographic transfer`
`evaluation methodology` `uncertainty quantification`

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
        Every multi-horizon urban growth benchmark I could find showed the same
        pattern: CNN accuracy drops at longer horizons, ConvLSTM improves. The
        standard explanation was architectural. It turns out 94% of that gap
        is a channel-count confound — advancing the horizon also removes an input
        epoch, and nobody had controlled for it. Tested across 5,698 CONUS tiles
        at 250m. The confound structure applies anywhere multi-horizon benchmarks
        shorten the encoder window as the target moves forward.
      </p>
      <p>
        <a href="https://github.com/rohanbalixz/Multi-Horizon-Urban-Growth-Prediction"><strong>Code & data</strong></a> ·
        <em>arXiv pending</em>
      </p>
    </td>
  </tr>
</table>

#### Key results

- Channel-matched CNN leads at every horizon. FoM 0.702 ± 0.019 on the 2015 spatial holdout; 0.252 ± 0.009 on a sealed 2020 temporal holdout.
- ConvLSTM's gain across horizons traces to a 5.4x asymmetric sensitivity to removing the most recent epoch, not a general long-horizon architectural advantage.
- MSE inverts model rankings algebraically when fewer than ~11% of pixels change. Derived formally. Soft-Jaccard training, which is nominally FoM-aligned, collapses to near-null predictions — 4.2x worse FoM than MSE training.
- Zero-shot transfer to Lagos, Nigeria (69.6% growth fraction): ConvLSTM falls below pixel-wise linear extrapolation. CNN degrades more gracefully. The gap connects back to recency anchoring in the hidden state.
- MC Dropout uncertainty correlates with actual error at r = 0.983 across decile bins (~8.7M pixels). Rank ordering is reliable; magnitudes are underestimated 1.4–1.9x and need post-hoc scaling before use as coverage bounds.

#### Venues

- **GeoAI 2026** — 9th ACM SIGSPATIAL International Workshop on Geospatial Artificial Intelligence. Oral presentation. Ghent, Belgium. November 2026.
- **SpatialDI 2026** — 7th International Conference on Spatial Data and Intelligence (ACM SIGSPATIAL China Chapter). Springer LNCS proceedings. Changsha, China. April 2026.

---

## Selected Projects

### Disaster Risk Monitoring from Satellite Radar
*NVIDIA Deep Learning Institute · Earth Observation Track*

U-Net trained on Sentinel-1 SAR imagery for flood-extent detection, with SAR-specific
preprocessing (speckle filtering, dB conversion, polarization-aware augmentation).
Dice 0.82, IoU 0.78. Inference pipeline integrated with Google Earth Engine.

Same core problem as the urban growth work: multitemporal satellite stacks,
sparse change signal, and a standard pipeline that doesn't account for
what makes geospatial data different.

[Repository](https://github.com/rohanbalixz/Disaster-Risk-Monitoring-Using-Satellite-Imagery)

### Small-World Structure in Academic Collaboration
*Advised by Prof. Dana S. Fine, University of Massachusetts Dartmouth*

Co-authorship networks across 12 academic fields, 180K+ edges. 72% of researchers
in the top citation percentile sit within 3 hops of each other in their field graph.
The structure has consequences for how ideas and opportunity move through science.

[Repository](https://github.com/rohanbalixz/Understanding-Academic-Collaboration-Networks-Through-Small-World-Theory)

---

## Currently

Working on causal modeling for land-cover change and figuring out where and why
spatiotemporal models fail when the geography shifts. Preparing follow-on submissions
and PhD applications for Fall 2027.

Open to collaborations in geospatial AI, earth observation ML, and spatiotemporal
representation learning.

<p align="left">
  <a href="mailto:rohanbaliwork@gmail.com">
    <img src="https://img.shields.io/badge/Email-rohanbaliwork@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>
