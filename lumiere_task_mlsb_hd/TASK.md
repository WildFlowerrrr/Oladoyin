# Project Lumière (Life Sciences): Petri Dishes & Culture Plates
## MLSB phenotypes by D-zone test: hazy-D (constitutive) vs D/D+ (inducible)

### Blind pre-test
| Run | Answer | Outcome |
|---|---|---|
| 1 (Opus) | 51 | Fail: panel b (hazy-D, cMLSB) read as D+ (iMLSB) |
| 2 (Opus) | 42 | Pass |
| 3 (Opus) | 51 | Fail: named panel b "hazy D" but classified it as inducible |
| **GTFA** | **42** | |

### Source
- DOI: https://doi.org/10.3390/antibiotics12030503
- Title: Inhibition of Erythromycin and Erythromycin-Induced Resistance among Staphylococcus aureus Clinical Isolates
- Antibiotics (MDPI), Volume 12, Issue 3, 2023, Article 503. CC BY 4.0.
- Image: Figure 3, uploaded whole and unedited (publisher full resolution 2522 × 2266 px).
- Caption identities: (a) R phenotype, cMLSB; (b) HD phenotype, cMLSB; (c) D phenotype, iMLSB; (d) D+ phenotype, iMLSB; (e) MS phenotype; (f) S phenotype.

### Prompt
```
Image 1 shows six panels (a–f), each a close-up of a Mueller-Hinton agar plate inoculated with a different clinical Staphylococcus aureus isolate and tested by the double-disk diffusion (D-zone) test with an erythromycin 15 µg disk (E 15) and a clindamycin 2 µg disk (DA 2) placed 15 mm apart (edge to edge), incubated for 24 h at 37 °C.

A hospital laboratory tests 120 S. aureus isolates in the same way; 14, 9, 31, 11, 23 and 32 of them reproduce the patterns shown in panels a, b, c, d, e and f, respectively. Each isolate is assigned to an MLSB phenotype from the appearance of its plate. How many of the 120 isolates are assigned the inducible MLSB (iMLSB) phenotype?

Report the answer as an integer (for example, 40).
```

### GTFA
```
42
```

See the chat for every other field in copy boxes.
