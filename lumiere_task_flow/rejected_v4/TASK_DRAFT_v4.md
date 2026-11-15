# Project Lumiere — Flow Cytometry task (Cell Biology) — DRAFT v4

**Status:** in-house test 1 of 2 models fail (Sonnet fails 2/2, Opus passes 3/3) — see "Test log".

## Source & licence
- **Image:** Image 1 — Panel A of Figure 4, cropped from the full figure (Panel B bar chart removed)
- **Article title:** Multiple Dendritic Cell Populations Activate CD4+ T Cells after Viral Stimulation
- **Authors:** Mount AM, Smith CM, Kupresanin F, Stoermer K, Heath WR, Belz GT
- **Where published:** PLoS ONE 3(2): e1691 (2008)
- **URL / DOI:** https://doi.org/10.1371/journal.pone.0001691 (Figure 4)
- **Licence text (publisher):** "This is an open-access article distributed under the terms of the Creative Commons Attribution License, which permits unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited." → **CC BY**
- Peer-reviewed and published; no BioRender; caption has no "reproduced/adapted from".
- Only modification: crop to Panel A (no resampling, sharpening or colour change).
- File: `Image1_CFSE_proliferation.png` — 2067 × 745 px PNG, 134 KB.
- The division count / inter-division time for this sample is not stated anywhere in the paper.

## Prompt (≈1,000 characters)
The image shows CFSE histograms of CFSE-labelled, influenza haemagglutinin-specific TCR-transgenic CD8$^+$ (CL4) and CD4$^+$ (HNT) T cells recovered from the draining popliteal lymph node 72 h after adoptive transfer into mice that had been infected with influenza virus 1, 2, 3, 4 or 5 days before the transfer ("Day 1" to "Day 5"); "Naive" denotes an uninfected recipient. The number in each histogram is the percentage of cells lying to the left of the dashed line.

For the HNT CD4$^+$ T cells transferred on Day 5, determine the most advanced division the responding cells reached during the 72 h, and use it to calculate the maximum possible average inter-division time (in hours) of the cells in that most-divided generation, assuming they were dividing throughout the entire 72 h period.

Report the time in hours to one decimal place (e.g., 7.5).

## Answer format
Decimal, 1 decimal place.

## GTFA
**9.0**

## Step-by-step solution
Step 1: Locate the histogram for HNT CD4$^+$ T cells transferred on Day 5: bottom row, fifth column (labelled 83.6).

Step 2: Identify the undivided population. In both "Naive" histograms, where the T cells receive no antigen, almost all events form one narrow spike at the far right (highest CFSE). In the Day 5 HNT histogram, the spike to the right of the dashed line sits at the same position, so it is the undivided (generation 0) population. The 83.6% to the left of the line are cells that have divided.

Step 3: Apply the dye-dilution principle. CFSE binds intracellular proteins covalently and is shared equally between the two daughter cells at each mitosis. Each division therefore halves the fluorescence, and on the log CFSE axis each generation appears as a discrete peak one constant step further left.

Step 4: Count the division peaks to the left of the undivided peak, from right to left:
- two low peaks just left of the dashed line (divisions 1 and 2)
- four tall peaks of similar height across the centre (divisions 3, 4, 5 and 6)
- one shorter peak (division 7)
- a small, low, rounded hump at the far left edge of the histogram (division 8)

Step 5: Check that the far-left hump is a real generation. It lies one peak spacing beyond division 7, the same spacing as between the other peaks. The whole span from the undivided peak to that hump is eight peak spacings. So the most advanced division reached is division 8.

Step 6: Cells in generation 8 have completed 8 divisions within the 72 h window. If they were dividing for the whole 72 h, the average time per division is 72 h / 8 = 9.0 h. Any lag before the first division would shorten the real inter-division time, so 9.0 h is the maximum possible average.

Final Answer: 9.0

## Image description (≥200 words; does not state the answer)
Modality: a composite of twelve flow-cytometry single-parameter histograms (solid black filled curves on a white background) arranged in two rows and six columns, labelled "A" at the top left.
- Row labels at the left read "CL4 CD8" (top) and "HNT CD4" (bottom).
- Column headings read "Day 1", "Day 2", "Day 3", "Day 4", "Day 5" and "Naive".
- A single long arrow along the bottom, labelled "CFSE", indicates fluorescence increasing to the right.
- No numeric axis scale, tick labels or y-axis title are shown. Each histogram has only a left vertical line and a baseline.
- Each histogram has a vertical dashed line near its right side and a number at its upper left: 92.2, 92.4, 95.1, 96.4, 95.4 and 11.3 in the top row; 93.7, 92.7, 93.3, 86.4, 83.6 and 8.13 in the bottom row.

Content:
- **Naive panels:** almost all events form one narrow, tall spike at the far right, to the right of the dashed line. The bottom Naive panel also has a tiny, flat bump far to the left.
- **Day 1–5 panels:** events spread leftward from that rightmost position as a comb of narrow spikes separated by troughs. A small spike sits immediately right of the dashed line, and further spikes continue to the left. Towards the left edge, neighbouring spikes increasingly overlap on a raised continuous base.
- **Top row:** each profile is dominated by two or three tall spikes towards the left-centre and ends in a steep left flank without separated spikes.
- **Bottom row, Days 1–3:** tall profiles whose left portion forms a dense merged block.
- **Bottom row, Days 4 and 5:** lower, broader profiles whose spikes are of more similar height.
- **Day 5 HNT CD4 histogram, right to left:**
  - one tall spike to the right of the dashed line
  - two low spikes just left of the line
  - four taller spikes of roughly equal height across the middle
  - one shorter spike
  - finally, at the far left edge, a small, low, rounded hump before the curve returns to the baseline
  - These spikes are roughly evenly spaced.

Quality: the curves are crisp at original resolution. Spike tips are sharp, but the leftmost spikes in most panels are partly merged, and the panels are small with no gridlines.

Artifacts and annotations: there are no colours, legends, scale bars or arrows other than the CFSE axis arrow. The only annotations are the row and column labels, the per-panel numbers, the dashed gate lines and the panel letter.

## Distractors (incorrect answers only)
Note that in testing we provided the model all potential answers, including the GTFA.
- **10.3:** misses the faint far-left hump and counts 7 divisions (72 / 7).
- **8.0:** counts the undivided peak as a division, giving 9 (72 / 9).
- **12.0:** counts 6 divisions by merging adjacent tall central peaks and missing the far-left hump (72 / 6). Observed in both platform model responses.
- **14.4:** counts 5 divisions, merging the closely spaced central peaks (72 / 5).
- **7.2:** counts 10 divisions, treating the dashed-line edge and a trough shoulder as extra peaks (72 / 10).

## Model failure (in-house)
- **Sonnet (2 of 2 runs):** final answer 10.3. It counted only 7 division peaks, missing the small rounded hump at the far left of the Day 5 HNT histogram (the 8th generation), and so computed 72/7. This is miscounting discrete populations in a dense histogram, a misreading of the image, not an arithmetic or reasoning slip.
  - Error type: Data extraction error (or Figure-based quantitative estimation error).
- **Opus (3 of 3 runs, single view, no zoom):** correct (9.0).

## Test log
| Version | Image | Opus | Sonnet |
|---|---|---|---|
| v1 | e48032 Fig 3 (Annexin V/PI, swapped axes) | ✔ 3.52 | ✔ 3.52 |
| v2 | e0347201 Fig 1 (B-ALL DNA index doublets), hinted | ✔ 1:1 | ✔ 1:1 |
| v3 | same image, unhinted ("second clone" claim) | ✔ 1:1 | ✔ 1:1 |
| v4 | e1691 Fig 4A (CFSE generations) | ✔ 9.0 ×3 | ✘ 10.3 ×2 |

## Lessons (do not repeat)
- Printed quadrant percentages plus clean axis labels mean the models just read them off. Avoid tasks whose only difficulty is reading printed numbers.
- Defining the populations in the prompt ("early apoptotic", "how many cells per event") turns the task into arithmetic. This also risks a DOMAIN_KNOWLEDGE_FLOOR flag.
- Strong models handle swapped axes and doublet logic well. Perceptual difficulty (dense or overlapping peaks, faint features) is what produces valid failures.

## Feedback received (platform checker)
- **FAILURE_BAR_NOT_MET (MAJOR), both blocks:** the checker judged the 6-vs-8 peak count a "bare misread" or "perceptual miscount, not biological misinterpretation". It was the same type of flag the PDF lists in Section 12 ("both models missed faint bands: judged a perceptual miss").
  - **Rule going forward:** never design a task whose only failure point is counting or detecting faint features. The model's error must come from interpreting what a feature *means* (biology, gating logic, artifact vs signal), not from how many features it sees.
