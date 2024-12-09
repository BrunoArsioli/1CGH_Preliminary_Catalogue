# Data Description: 1CGH Catalogue Columns

This document provides detailed explanations for each column included in the 1CGH catalogue. The catalogue represents a dataset compiled using 16 years of Fermi-LAT observations (August 2008 to August 2024) and includes information for all gamma-ray sources detected above 10 GeV.

### Column Definitions

| **Column Name**           | **Description**                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1CGH_name**             | The source identifier, formatted as `1CGHJ0123+0123`, based on the sexagesimal J2000 coordinates. Includes four digits each for R.A. and Dec. For associated sources, the R.A. and Dec. correspond to the optical, infrared, or radio counterpart. For unassociated sources, these coordinates are derived from gamma-ray astrometry as reported in 4FGL-DR4. |
| **RA_1CGH**               | Right Ascension (J2000) of the counterpart or gamma-ray source in degrees.                                                                                                                                                                                                                                                                                       |
| **DEC_1CGH**              | Declination (J2000) of the counterpart or gamma-ray source in degrees.                                                                                                                                                                                                                                                                                           |
| **Counterpart_name**      | The name of the source in the main catalogues used to build the candidate list. This includes names from 5BZcat, 3HSP, Maselli, Paliya, TeVcat, and 4FGL-DR4.                                                                                                                                                                                                    |
| **N0[1E-16]**             | Normalization constant (prefactor) of the power-law fit in units of photons/cm²/s/MeV, calculated at the pivot energy.                                                                                                                                                                                                                                           |
| **N0_err[1E-16]**         | Uncertainty in the normalization constant.                                                                                                                                                                                                                                                                                                                       |
| **Index**                 | Photon spectral index of the power-law model.                                                                                                                                                                                                                                                                                                                    |
| **Index_err**             | Uncertainty in the photon spectral index.                                                                                                                                                                                                                                                                                                                        |
| **Flux[1E-12]**           | Integrated photon flux in the 10–800 GeV range, in units of photons/cm²/s.                                                                                                                                                                                                                                                                                       |
| **Flux_err[1E-12]**       | Uncertainty in the integrated photon flux.                                                                                                                                                                                                                                                                                                                       |
| **TS**                    | Test Statistic value for the source detection, indicating the significance of the detection.                                                                                                                                                                                                                                                                     |
| **z**                     | Redshift of the source.                                                                                                                                                                                                                                                                                                                                          |
| **zflag**                 | Redshift reliability flag: (1) robust spectroscopic, (2) photometric/uncertain, (3) lower limit.                                                                                                                                                                                                                                                                 |
| **z_origin**              | Reference for the redshift, tracking its origin in the literature or catalogues (e.g., 5BZcat, 3HSP, observation campaigns as reported in the paper).                                                                                                                                                                                                             |
| **Nph_128**               | Number of photons associated with the source when using `evclass=128` (Source_type events).                                                                                                                                                                                                                                                                     |
| **Emax_128[GeV]**         | Maximum photon energy detected for `evclass=128` (Source_type events).                                                                                                                                                                                                                                                                                          |
| **Nph_512**               | Number of photons associated with the source when using `evclass=512` (UltraClean_type events).                                                                                                                                                                                                                                                                 |
| **Emax_512[GeV]**         | Maximum photon energy detected for `evclass=512` (UltraClean_type events).                                                                                                                                                                                                                                                                                      |
| **Ebin_max[GeV]**         | Mean energy of the four highest-energy photons detected for the source (using `evclass=128`). This represents the largest energy bin detectable with Fermi-LAT.                                                                                                                                                                                                  |
| **TransmissionEbin**      | Flux transmission factor at \($E_{max}^{bin}$\) , calculated as \($e^{-\tau_{(E,z)}}$\). The EBL model by Saldana-Lopez (2021) is used as a reference framework.                                                                                                                                                                                                             |
| **AbsEbin**               | Flux absorption factor at \($E_{max}^{bin}$\) , calculated as \(1 - TransmissionEbin\).                                                                                                                                                                                                                                                                             |
| **tauEbin**               | EBL optical depth (\($\tau$\)) at \($E_{max}^{bin}$\), based on Saldana-Lopez (2021).                                                                                                                                                                                                                                                                                      |
| **Abs_flag**              | Absorption flag: (1) for cases where \($\tau > 0.1$\), indicating moderate to severe attenuation; (0) for cases where \($\tau \leq 0.1$\), indicating negligible attenuation.                                                                                                                                                                                                                        |
| **GAL_LAT**               | Galactic latitude of the source in degrees.                                                                                                                                                                                                                                                                                                                      |
| **BZcat**                 | Identifier in the 5BZcat catalogue, if available.                                                                                                                                                                                                                                                                                                                |
| **z_3HSP**                | Redshift of the source as reported in the 3HSP catalogue, if available.                                                                                                                                                                                                                                                                                          |
| **zflag_3HSP**            | Redshift flag as defined in the 3HSP catalogue.                                                                                                                                                                                                                                                                                                                  |
| **4FGL_counter_name**     | Counterpart name reported in the 4FGL-DR4 catalogue.                                                                                                                                                                                                                                                                                                             |
| **TEVCAT_FLAG_4FGLdr4**   | Indicates if the source is flagged in the TeVCat catalogue, as per 4FGL-DR4.                                                                                                                                                                                                                                                                                     |
| **ASSOC_TEV_4FGLdr4**     | Association of the source with TeV detections, as reported in 4FGL-DR4.                                                                                                                                                                                                                                                                                          |
| **CLASS1_4FGLdr4**        | Classification of the source in 4FGL-DR4 (e.g., blazar, pulsar, unassociated).                                                                                                                                                                                                                                                                                   |
| **ASSOC1_4FGLdr4**        | Counterpart name in 4FGL-DR4, if available.                                                                                                                                                                                                                                                                                                                       |
| **Name_4LACdr3**          | Counterpart name reported in the 4LAC-DR3 catalogue, if available.                                                                                                                                                                                                                                                                                               |
| **z_4LACdr3_1**           | Redshift as reported in the 4LAC-DR3 catalogue.                                                                                                                                                                                                                                                                                                                  |
| **Name_3FHL**             | Counterpart name reported in the 3FHL catalogue, if available.                                                                                                                                                                                                                                                                                                   |
| **z_3FHL**                | Redshift as reported in the 3FHL catalogue.                                                                                                                                                                                                                                                                                                                      |

---

If you have further questions, feel free to contact the authors or refer to the published paper for additional context.

---
