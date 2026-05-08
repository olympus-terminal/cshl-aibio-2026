# Genome-Environment Coupling Across 221 Million Algal Sequences

**Full figure legends for the poster presented at the CSHL 90th Symposium — AI in Biology (2026)**

David Roy Nelson<sup>1,3,*</sup>, Sarah Daakour<sup>1</sup>, Maxence Plouviez<sup>2</sup>, and Kourosh Salehi-Ashtiani<sup>1</sup>

<sup>1</sup>Division of Science, New York University Abu Dhabi
<sup>2</sup>Cawthron Institute, Nelson, New Zealand
<sup>3</sup>Lead contact &nbsp; <sup>*</sup>drn2@nyu.edu

---

## Poster Figures and Full Legends

The poster presents six multi-panel figures from the manuscript. Abbreviated captions appear on the poster; full legends with panel-level detail are provided below.

---

### Figure 2: Basin coverage, AlgaGPT classification, and environment-genome manifold structure

*Poster panels shown: A-I*

**(A)** Global distribution of 1,810 geolocated samples across seven ocean basins. **(B)** Depth distribution by basin (violin plots, log scale). **(C)** AlgaGPT sequence retention rates across five data source categories. **(D)** RuBisCO large-subunit lineage composition across 3,743 hits from 10 algal lineages, colored by photosynthetic lineage (green = Form IB; blue = Form ID). **(E)** AlgaGPT three-class classification breakdown (algae, contamination, unknown) by data source type. **(F)** Distribution of AlgaGPT retention percentages by source type. **(G-I)** UMAP of PFAM domain abundance (20,318 domains, 1,523 samples), colored by temperature (G), chlorophyll-a (H), and depth (I). Gray: missing metadata.

---

### Figure 3: Canonical correlation manifold, environment-genome associations, and CCA nonlinearity

*Poster panels shown: A-T*

**(A)** UMAP of 10-component CCA embeddings (963 of 995 samples; 32 outliers removed by IQR filter), colored by dominant canonical component: red = CC1, teal = CC2, blue = CC3. Saturation encodes dominance strength. **(B)** Environmental loadings on CC1-CC3 (top 12 variables by absolute loading). **(C)** Pearson correlation heatmap: 6 environmental variables x 10 canonical components, hierarchically clustered. Dot size encodes significance (p < 0.05, < 0.01, < 0.001); color scale: diverging, +/-0.6. **(D)** CC1 density by dominant RuBisCO lineage. **(E)** Observed canonical correlations versus permutation null (1,000 shuffles; gray band = +/-2 SD); CC1 p < 0.001. **(F)** Reverse-model R2 (PFAM -> environment) for targets with R2 > 0.1. **(G)** KAN-CCA versus linear CCA test correlations (10-fold spatial block CV; k = 13 sparse features). KAN-CCA improves CC2 and CC3 (p < 0.01), not CC1. **(H)** Ablation across sparsity levels: KAN (solid) versus linear (dashed) CCA for CC1-CC3. **(I-N)** Learned B-spline activation functions for the six top-weighted domain features (KAN-CCA, CC1). Gray: individual folds; colored: mean. R2 = linearity of spline (lower = more nonlinear). **(O-S)** Learned B-spline activations for the five top-weighted environmental features. **(T)** Legend panel.

---

### Figure 4: Modular organization of domain-environment coupling

*Poster panels shown: A-E*

**(A)** K-means biclustered heatmap of Spearman rho: 384 PFAM domains (mean normalized |SHAP| >= 5% of max) clustered at k = 8 across 29 environmental variables; the top 30 per cluster are displayed for readability (191 rows shown). Left marginal: SHAP importance; right annotations: dominant environmental association per cluster; bottom: reverse-model R2 per variable. **(B)** Top 15 domains by mean SHAP importance. Inner ring: cluster membership; outer ring: SHAP magnitude. **(C)** Sankey diagram from importance tiers through clusters to environmental categories. Flow width proportional to domain-variable associations. **(D)** Sensitivity of reverse-model R2 to exclusion of transposase-family domains (bathymetry and SST targets). Bars compare the full feature set to the TE-excluded set; labels show absolute delta R2. **(E)** Bootstrap 95% confidence intervals on reverse-model R2 per environmental variable (1,000 resamples; 80/20 split). Horizontal lines: 95% CI; points: bootstrap point estimates; colors indicate environmental category.

---

### Figure 6: Forward model calibration and prediction accuracy distribution

*Poster panels shown: A-H*

**(A-F)** Observed versus predicted CLR-transformed PFAM abundance (10-fold spatial block CV, n = 1,878; satellite-only environmental features) for the six most predictable domains: DUF6570 (R2 = 0.586), Helitron_like_N (0.496), Phage_integrase (0.495), PIF1 (0.483), RNase_H (0.423), Ice_binding (0.366). Hexbin density; dashed line = identity. **(G)** Forward R2 distribution across 9,989 domains: 65 (0.7%; fold-bootstrap 95% CI: 51-118) exceed R2 > 0.3; 74.5% exceed R2 > 0 (versus ~5% expected under permutation null). **(H)** Top 100 domains by forward R2; dotted line: top-18 cutoff; dashed: R2 = 0.3.

---

### Figure 7: Novel domain discovery, structural validation, and sensitivity analysis

*Poster panels shown: A-H*

**(A)** Cluster size distribution after MMseqs2 linclust at 30% identity (122.1M clusters; power-law alpha = -3.06). Vertical line: >= 10 member threshold (33,950 HMMs). **(B)** Novel domain prevalence across 2,044 assemblies (hmmsearch E < 1e-9, Pfam-equivalent primary threshold); dashed line: median. **(C)** Environmental coupling: novel versus Pfam domains at E < 1e-9 (FDR < 0.05). Novel: 73.5% significant, median |rho| = 0.179; Pfam: 45.7%, median |rho| = 0.070. Under a matched design (same 1,523 samples, same 18 variables), the enrichment is 2.29-fold (bootstrap 95% CI [2.28, 2.30]). **(D)** Cluster size versus prevalence for 33,950 domains, colored by source type. **(E)** Dark fraction by source category: median (solid) and mean +/- SD (translucent) Pfam-dark percentage across ocean metagenomes (TARA + OSD), MMETSP transcriptomes, and cultured reference proteomes. Dashed line: global median (83.7%). **(F)** Novel domain prevalence by source type (violin/box). **(G)** Significance rates (FDR < 0.05) for Pfam and novel domains at each E-value threshold. **(H)** ESMFold pLDDT per-residue profiles for the ten highest-ranked novel domains; dashed line at pLDDT = 70 (7/10 domains above).

*Panels I-K (not shown on poster):* (I) Foldseek structural-search best hits against PDB and AlphaFold Database: heatmap cells show TM-score (blank = no hit at E < 1e-3); 5/10 domains have no match in either database. (J) Effect size distributions (|rho|) across thresholds. (K) Significance enrichment across thresholds.

---

## Related Resources

- **LA4SR Paper:** Nelson et al. (2025) *Patterns* 6, 101373. [DOI: 10.1016/j.patter.2025.101373](https://doi.org/10.1016/j.patter.2025.101373)
- **Models:** [HuggingFace — GreenGenomicsLab](https://huggingface.co/GreenGenomicsLab)
- **Code:** [GitHub — olympus-terminal](https://github.com/olympus-terminal)
- **Data:** Zenodo [10.5281/zenodo.18538439](https://doi.org/10.5281/zenodo.18538439)

## Citation

> Nelson, D.R., Daakour, S., Plouviez, M., and Salehi-Ashtiani, K. (2026). Protein language models and satellite embeddings reveal genome-environment coupling across 221 million algal sequences. Poster presented at the CSHL 90th Symposium — AI in Biology.

## License

This repository is provided for academic reference. The underlying data and methods are described in the associated publications.
