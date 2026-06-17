# Rohan Bali

I'm an M.S. Data Science student at the University of Massachusetts Dartmouth. I work on how machine learning models for satellite and Earth data get tested, and whether they hold up once the region or the data changes.

A lot of papers say one model beats another. I spend most of my time checking whether that is actually true, because the win often comes from how the data was set up rather than from the model. So I take benchmarks apart and see how much of a result is still there once the test gets harder. Right now that is urban growth prediction, cross-region transfer, and uncertainty under shift. I am applying to PhD programs for Fall 2027.

[Website](https://rohanbalixz.github.io/rohan-bali-portfolio/) · [Google Scholar](https://scholar.google.com/citations?user=CBgU9IIAAAAJ&hl=en) · [ORCID](https://orcid.org/0009-0001-9880-3906) · [OpenReview](https://openreview.net/profile?id=~Rohan_Bali1) · [LinkedIn](https://www.linkedin.com/in/rohan-bali-301345293/) · rbali@umassd.edu

## Papers

**The Channel-Count Confound: A Continental Audit of Multi-Horizon Urban Growth Prediction**  
SpatialDI 2026 (Springer LNCS), and GeoAI 2026 as an oral. Sole author.

People keep reporting that ConvLSTMs beat plain CNNs at predicting urban growth further into the future. I checked that across 305M pixels of the continental US. Once you seal the 2020 holdout, test cold on Lagos, and calibrate the uncertainty over 8.69M pixels, the ConvLSTM lead at longer horizons mostly goes away. About 94% of it came from the number of input channels, not from the model learning anything better.

<img src="https://raw.githubusercontent.com/rohanbalixz/Multi-Horizon-Urban-Growth-Prediction/main/results/figures/fig7_uncertainty.png" width="720" alt="A held-out tile showing GHSL ground truth, the ConvLSTM prediction, and MC Dropout uncertainty over 20 stochastic forward passes.">

*A Mid-Atlantic held-out tile. From left: GHSL ground truth, the ConvLSTM prediction, and MC Dropout uncertainty over 20 stochastic forward passes.*

**What I found**

- The channel-matched CNN leads at every horizon. It reaches FoM 0.702 (plus or minus 0.019) on the 2015 spatial holdout and 0.252 (plus or minus 0.009) on a sealed 2020 temporal holdout.
- The ConvLSTM's edge across horizons traces back to one thing. It is 5.4 times more sensitive to dropping the most recent epoch than to dropping a mid-sequence one. That is recency anchoring, not a real long-horizon advantage.
- MSE flips the model rankings on its own once fewer than about 11% of pixels change, which I derive formally. Soft-Jaccard training is supposed to line up with FoM, but it collapses to almost-null predictions and scores 4.2 times worse on FoM than plain MSE training.
- On a cold transfer to Lagos, Nigeria, where 69.6% of pixels grew, the ConvLSTM drops below a simple pixel-wise linear extrapolation while the CNN degrades more gently. The gap comes back to that same recency anchoring in the hidden state.
- MC Dropout uncertainty tracks actual error at r = 0.983 across decile bins, over about 8.7M pixels. The ranking is reliable, but the magnitudes come out 1.4 to 1.9 times too small and need post-hoc scaling before you use them as coverage bounds.

[Code and data](https://github.com/rohanbalixz/Multi-Horizon-Urban-Growth-Prediction) · [PDF](https://zenodo.org/records/20278403)

**Train Anywhere, Test Everywhere: Cross-Region Transfer in Earth Observation Is Decided by the Data, Not the Model**  
In progress, aimed at SIGSPATIAL 2026. Sole author.

I trained one model per region and tested every model on every region across twenty regions. The training source barely matters. The test region sets the score, and a one-line rule that just extends each region's recent past beats every trained model. Change the input instead and transfer falls along a spectrum, from harmonized products that carry over to raw reflectance that hardly does. The same pattern shows up again on the published PANGAEA benchmark.

[Code and data](https://github.com/rohanbalixz/Cross-Region-Source-Invariance-in-Earth-Observation)

**UrbanFinance: Forecasting the Latent Land-Demand Residual across Divergent Indian Metros**  
In progress. Sole author.

Instead of predicting built-up area or price, this one goes after the gap between where the demand for land is and where building actually happened, across five very different Indian metros. The model holds up better than the usual baselines, and when a whole city is held out it still transfers to that unseen city.

## A few other things

**Disaster Risk Monitoring from Satellite Radar** (NVIDIA Deep Learning Institute). A U-Net for flood detection on Sentinel-1 SAR, with preprocessing tuned to radar noise. Dice 0.82, IoU 0.78, wired into Google Earth Engine. [Repository](https://github.com/rohanbalixz/Disaster-Risk-Monitoring-Using-Satellite-Imagery)

**Small-World Structure in Academic Collaboration**. Co-authorship networks across 12 fields and more than 180,000 edges. About 72% of the most-cited researchers sit within three hops of each other in their field. [Repository](https://github.com/rohanbalixz/Understanding-Academic-Collaboration-Networks-Through-Small-World-Theory)

## Currently

Figuring out where and why these models fall apart when the geography shifts, and getting the next papers and my PhD applications ready for Fall 2027. Based in Boston, MA. Happy to hear from anyone working on evaluation, generalization, uncertainty, or machine learning for Earth observation.

rbali@umassd.edu
