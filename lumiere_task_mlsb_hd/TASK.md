# Project Lumière (Life Sciences): Petri Dishes & Culture Plates
## MLSB phenotypes by D-zone test: hazy-D (constitutive) vs D/D+ (inducible)

### Blind pre-test
| Run | Answer | Outcome |
|---|---|---|
| 1 (Opus) | 51 | Fail: panel b (hazy-D, cMLSB) read as D+ (iMLSB) |
| 2 (Opus) | 42 | Pass |
| 3 (Opus) | 51 | Fail: named panel b "hazy D" but classified it as inducible |
| **GTFA (v1)** | **42** | |

v1 was flagged FAILURE_BAR_NOT_MET on the platform (models answered 40).

### Blind pre-test, v2 (scheme stated, constitutive count)
| Run | Answer | Outcome |
|---|---|---|
| 1 | 49 | Pass |
| 2 | 27 | Fail: b called D+, d called HD |
| 3 | 27 | Fail: b called D+, d called HD |
| **GTFA (v2)** | **49** | |

### Source
- DOI: https://doi.org/10.3390/antibiotics12030503
- Title: Inhibition of Erythromycin and Erythromycin-Induced Resistance among Staphylococcus aureus Clinical Isolates
- Antibiotics (MDPI), Volume 12, Issue 3, 2023, Article 503. CC BY 4.0.
- Image: Figure 3, uploaded whole and unedited (publisher full resolution 2522 × 2266 px).
- Caption identities: (a) R phenotype, cMLSB; (b) HD phenotype, cMLSB; (c) D phenotype, iMLSB; (d) D+ phenotype, iMLSB; (e) MS phenotype; (f) S phenotype.

### Prompt (v2: constitutive count, scheme stated)
```
Image 1 shows six panels (a–f), each a close-up of a Mueller-Hinton agar plate inoculated with a different clinical Staphylococcus aureus isolate and tested by the double-disk diffusion (D-zone) test with an erythromycin 15 µg disk (E 15) and a clindamycin 2 µg disk (DA 2) placed 15 mm apart (edge to edge), incubated for 24 h at 37 °C.

A hospital laboratory tests 120 S. aureus isolates in the same way; 12, 37, 18, 15, 16 and 22 of them reproduce the patterns shown in panels a, b, c, d, e and f, respectively. Each isolate is assigned to an MLSB phenotype from the appearance of its plate, using the D-test scheme in which the R and HD (hazy-D) phenotypes are constitutive MLSB (cMLSB), the D and D+ phenotypes are inducible MLSB (iMLSB), and the MS and S phenotypes are neither. How many of the 120 isolates are assigned a constitutive MLSB (cMLSB) phenotype?

Report the answer as an integer (for example, 40).
```

### GTFA
```
49
```

See the chat for every other field in copy boxes.
