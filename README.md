# Rohan Bali

Spatio-temporal machine learning · urban systems · computational social science

I build and evaluate models for complex spatio-temporal systems — urban growth, elections, collaboration networks — with a focus on what learned representations actually capture, where evaluation metrics fail, and how predictions transfer to regimes they were never trained on.

M.S. Data Science, University of Massachusetts Dartmouth (2024–2026).
Applying to PhD programs in computer science and societal computing, Fall 2027 entry.
Boston, MA.

[Portfolio](https://rohanbalixz.github.io/rohan-bali-portfolio/) · [Google Scholar](https://scholar.google.com/citations?user=CBgU9IIAAAAJ&hl=en) · [LinkedIn](https://www.linkedin.com/in/rohan-bali-301345293/) · [Twitter / X](https://x.com/bali2ro) · rohanbaliwork@gmail.com

---

## Research Interests

Spatio-temporal machine learning · Graph neural networks · Computational social science · Distribution shift and geographic transfer · Evaluation methodology for spatial forecasting · Machine learning for cities, elections, and public policy

---

## Selected Work

### Channel Count, Not Horizon Length, Drives Architectural Divergence in Multi-Horizon Urban Growth Prediction
**Solo-authored. GeoAI 2026 — Oral presentation (Ghent, Belgium).**

A controlled isolation experiment across **5,698 CONUS tiles** showing that **94% of the apparent architectural advantage** of recurrent encoders over convolutional ones at longer urban-growth forecast horizons is a **channel-count confound**, not a property of the architecture. The confound is present in every prior multi-horizon urban-growth benchmark I could identify.

- Channel-matched CNN leads at every horizon (FoM 0.702 ± 0.019 on the 2015 spatial holdout; 0.252 ± 0.009 on a sealed 2020 temporal holdout).
- ConvLSTM's multi-horizon gain isolated to a **5.4× asymmetric sensitivity** to terminal-epoch removal — consistent with recency anchoring, not general long-horizon capacity.
- Algebraic derivation showing MSE inverts model rankings at growth fractions below ~11%; FoM is the only operative ranking metric in this regime. Soft-Jaccard training (FoM-aligned) collapses to a near-null predictor — a 4.2× degradation versus MSE training.
- Zero-shot transfer to Lagos, Nigeria (20 tiles, 69.6% growth fraction): recency-anchored ConvLSTM transfers below pixel-wise linear extrapolation; flat-channel CNN degrades gracefully.
- MC Dropout uncertainty calibrated against empirical error at r = 0.983 across decile bins; magnitudes underestimated 1.4–1.9×, rank ordering reliable.

[Code, weights, and benchmark](https://github.com/rohanbalixz/Multi-Horizon-Urban-Growth-Prediction) · [Original NeuralTimeCapsule repository](https://github.com/rohanbalixz/NeuralTimeCapsule)

---

### Real-Time Election Forecasting — Bihar 2025
A streaming forecasting pipeline for the 2025 Bihar state-assembly election combining transformer-based sentiment analysis of news and social signals with Bayesian hierarchical priors over historical assembly-level voting data. Sub-5-minute update latency on streaming ingestion.

Stack: PyTorch · RoBERTa · NGBoost · XGBoost · Kafka.

[Repository](https://github.com/rohanbalixz/Bihar-Election-Analytics)

---

### Small-World Structure in Academic Collaboration
Co-authorship networks constructed and analyzed across 12 academic fields, totaling 180K+ edges. Finding: **72% of researchers in the top citation percentile sit within a 3-hop neighborhood** of one another in their respective field graphs — with implications for how reputation, ideas, and opportunity propagate through scientific communities.

[Repository](https://github.com/rohanbalixz/Understanding-Academic-Collaboration-Networks-Through-Small-World-Theory)

---

### Disaster Risk Monitoring from Satellite Radar
U-Net trained on Sentinel-1 synthetic-aperture-radar imagery for flood-extent detection, with SAR-specific preprocessing (speckle filtering, dB conversion, polarization-aware augmentation). Dice 0.82, IoU 0.78. Inference pipeline integrated with Google Earth Engine. Completed as the capstone of the NVIDIA Deep Learning Institute disaster-monitoring track.

[Repository](https://github.com/rohanbalixz/Disaster-Risk-Monitoring-Using-Satellite-Imagery)

---

## Currently

Extending the multi-horizon work toward causal urban-growth modeling and characterizing where predictive models systematically fail across geographies. Preparing follow-on submissions and PhD applications for Fall 2027.

Open to collaborations in spatio-temporal ML, network science, and computational social systems.

rohanbaliwork@gmail.com
