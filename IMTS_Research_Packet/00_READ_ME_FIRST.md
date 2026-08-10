# POSM Synthetic Intermodulation Transfer Spectroscopy Research Packet

**Prepared:** 2026-08-10  
**Working paper title:** *Synthetic Intermodulation Transfer Spectroscopy for Engineered Atomic Frequency Discrimination*

## Start here

1. **`Synthetic_IMTS_Theory_Packet_POSM.pdf`** - 19-page detailed theory / novelty / experiment packet.
2. **`literature/READING_LIST.md`** - organized, annotated high-recall literature map with primary links and novelty notes.
3. **`literature/open_access/`** - 16 open/preprint/government PDFs gathered for direct reading.
4. **`literature/patents/CN122178176A_CLOSEST_PRIOR_ART.md`** - closest 2026 dual-frequency MTS patent summarized and distinguished from proposed S-IMTS.
5. **`source_context/`** - the current POSM FPGA-lock, polarization-monitor, and packet-template PDFs used to keep the proposal grounded in the actual system.
6. **`figures/`** - packet figures, including a two-tone optical sideband lattice and illustrative channel/frequency-information plots.
7. **`docs/IMTS_Theory_Packet.tex`** - editable LaTeX source for the theory packet.

## Core hypothesis

Drive MTS with two coherent RF tones. Instead of demodulating only at the two fundamentals, inspect true combination-frequency channels

`p f1 + q f2`

including the difference, sum, and IM3-style products `2f1-f2` and `2f2-f1`. Treat the I/Q components of all useful channels as one multichannel measurement of laser detuning. If the channels contain complementary information, combine them with measured noise-covariance-aware weights to produce a synthetic discriminator with lower equivalent frequency noise or another engineered property.

## Recommended paper focus

**Primary result:** demonstrate more usable frequency information / lower equivalent frequency noise than the best conventional single-channel MTS baseline under equal optical and RF budgets.

**Secondary result:** demonstrate one engineered property unavailable from any individual channel, preferably steep local sensitivity plus a broader monotonic capture region.

**Tertiary result:** close the laser lock using the synthetic discriminator and compare conventional single-tone MTS, two-fundamental dual-frequency MTS, the best individual IM channel, and S-IMTS.

## Critical novelty boundary

Do **not** claim novelty for:
- using two modulation frequencies in MTS;
- adding two fundamental MTS error signals;
- two-tone FM / low-IF readout;
- multi-frequency optical MTS generally;
- synthetic modulation generally.

The proposed gap is specifically **atomically resonant combination-frequency output channels + joint complex/covariance-aware discriminator synthesis**. The packet treats this as a promising gap, not a proven “first.”

## Fast go/no-go test

Before building new lock firmware, use the raw RF channel to map complex probe response at low-order combination frequencies during a slow Rb scan. Run off-resonance, pump-blocked, overlap-removed, modulation-scaling, and phase-law controls. If no clean atomically dependent IM channels exist, stop early. If they do, immediately measure the local channel slope vector and noise covariance and perform the information audit.

## Copyright / access note

The literature folder intentionally does not contain publisher-only papers or papers for which a located repository copy explicitly restricted redistribution. Those works are still indexed with primary links in `READING_LIST.md`. This packet is a research handoff, not a legal freedom-to-operate or patent opinion.
