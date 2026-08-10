# CN122178176A - Closest Dual-Frequency MTS Patent Prior Art

**Publication:** CN122178176A  
**Applicant:** Zhejiang Sci-Tech University  
**Publication date:** 2026-06-09  
**Public summary:** https://eureka.patsnap.com/patent-CN122178176A

## What it does

- Drives an EOM with two modulation frequencies; its worked example uses 6 MHz and 9 MHz.
- Digitizes the detected spectroscopy signal.
- In FPGA, quadrature-demodulates at f1 and f2 independently.
- Low-pass filters to obtain two conventional fundamental-frequency error signals e1 and e2.
- Adds e1 + e2 to create a dual-frequency error signal.
- Optimizes modulation depths so the combined signal improves both zero-crossing slope and peak-to-peak amplitude relative to the best single-frequency cases.

The public description reports, for one simulation operating point, a peak-to-peak increase of 24.3% and slope increase of 8.6% relative to its 6 MHz maximum-slope single-frequency case; relative to its 9 MHz maximum-amplitude case, the combined slope is much larger.

## What it does NOT appear to establish

Based on the public claims/description reviewed on 2026-08-10, it does not appear to:

- demodulate at true combination frequencies p f1 + q f2 such as 2f1-f2 / 2f2-f1;
- identify atomically resonant intermodulation channels as independent measurements;
- form a covariance-aware multichannel minimum-noise frequency estimator;
- synthesize a discriminator under constraints such as RAM-insensitivity or target global line shape;
- quantify how much frequency information resides outside the two fundamental MTS components.

## Consequence for POSM novelty framing

Do not claim novelty for “dual-frequency MTS,” “adding two MTS error signals,” or “using two modulation depths to improve slope + amplitude.” The proposed S-IMTS paper must specifically test and exploit **true IM/combination-frequency output channels** and/or the **optimal multichannel synthetic discriminator**.

This is a research note, not a legal freedom-to-operate opinion.
