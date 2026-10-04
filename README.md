# TMEM106B-Structural-PPI-Analysis
Structural analysis of the TMEM106B protein–protein interface using PDB 9GI8 and PyMOL.

## Project Structure

tmem106b-structural-ppi-analysis/
│
├── README.md
│
├── report/
[Structural Analysis of TMEM106B Protein–Protein Interaction.pdf](https://github.com/user-attachments/files/33030623/Structural.Analysis.of.TMEM106B.Protein.Protein.Interaction.pdf)

│
├── figures/
│   ├── TMEM106B_9GI8_structure.png   <img width="658" height="537" alt="ChatGPT Image Oct 4, 2026, 09_50_15 PM" src="https://github.com/user-attachments/assets/16bede6b-3989-43ed-9f9c-f52ab0bcbc61" />

│   └── TMEM106B_interface.png    <img width="566" height="457" alt="ChatGPT Image Oct 4, 2026, 09_50_05 PM" src="https://github.com/user-attachments/assets/c85812c9-6f56-4030-a861-46f5b25cc42d" />
│
├── pymol/
│   └── TMEM106B_9GI8_analysis.txt
TMEM106B Structural PPI Analysis
PDB: 9GI8
Software: PyMOL

Reproducibility commands
========================

get_chains 9GI8

select TMEM106B_A_contact, 9GI8 and chain A within 4 of (9GI8 and chain B)
count_atoms TMEM106B_A_contact

select TMEM106B_A_iface, byres TMEM106B_A_contact
count_atoms TMEM106B_A_iface

select TMEM106B_B_contact, 9GI8 and chain B within 4 of (9GI8 and chain A)
count_atoms TMEM106B_B_contact

select TMEM106B_B_iface, byres TMEM106B_B_contact
count_atoms TMEM106B_B_iface


3.5 Å close-contact analysis
============================

select TMEM106B_A_close35, 9GI8 and chain A within 3.5 of (9GI8 and chain B)
count_atoms TMEM106B_A_close35

select TMEM106B_B_close35, 9GI8 and chain B within 3.5 of (9GI8 and chain A)
count_atoms TMEM106B_B_close35


Distance visualization
======================

distance TMEM106B_AB_close, (9GI8 and chain A), (9GI8 and chain B), 3.5, 0

show labels, TMEM106B_AB_close


Residue atom inspection
=======================

iterate 9GI8 and chain A and resi 54, print(name)


Structural validation control
=============================

get_distance (9GI8 and chain A and resi 54 and name OG1), (9GI8 and chain B and resi 54 and name OG1)

Observed distance:

THR54(A) OG1 → THR54(B) OG1 = 40.440 Å


│
└── results/
    └── interface_residues.txt
    TMEM106B Structural PPI Interface Results
PDB: 9GI8
Chains: A and B


4 Å INTERFACE ANALYSIS
======================

Chain A
-------
Contact atoms: 547
Residue-expanded interface atoms: 592
CA-defined interface residues: 38

Interface residues:

54 THR
55 GLY
56 ARG
57 ASP
58 SER
59 VAL
60 THR
61 CYS
62 PRO
63 THR
64 CYS
65 GLN
66 GLY
68 GLY
69 ARG
70 ILE
71 PRO
72 ARG
73 GLY
74 GLN
75 GLU
76 ASN
77 GLN
78 LEU
79 VAL
80 ALA
81 LEU
82 ILE
83 PRO
84 TYR
85 SER
86 ASP
87 GLN
88 ARG
89 LEU
90 ARG
91 PRO
92 ARG


Chain B
-------
Contact atoms: 499
Residue-expanded interface atoms: 591
CA-defined interface residues: 38

Interface residues:

54 THR
55 GLY
56 ARG
57 ASP
58 SER
59 VAL
60 THR
61 CYS
62 PRO
63 THR
64 CYS
65 GLN
66 GLY
68 GLY
69 ARG
70 ILE
71 PRO
72 ARG
73 GLY
74 GLN
75 GLU
76 ASN
77 GLN
78 LEU
79 VAL
80 ALA
81 LEU
82 ILE
83 PRO
84 TYR
85 SER
86 ASP
87 GLN
88 ARG
89 LEU
90 ARG
91 PRO
92 ARG


3.5 Å CLOSE-CONTACT ANALYSIS
============================

Chain A
-------
Close-contact atoms: 506
CA-defined close-contact residues: 29

Residues:

54 THR
55 GLY
56 ARG
57 ASP
61 CYS
62 PRO
66 GLY
68 GLY
69 ARG
70 ILE
71 PRO
72 ARG
76 ASN
77 GLN
78 LEU
79 VAL
80 ALA
81 LEU
82 ILE
83 PRO
84 TYR
85 SER
86 ASP
87 GLN
88 ARG
89 LEU
90 ARG
91 PRO
92 ARG


Chain B
-------
Close-contact atoms: 466
CA-defined close-contact residues: 26

Residues:

54 THR
55 GLY
56 ARG
57 ASP
61 CYS
62 PRO
66 GLY
68 GLY
69 ARG
70 ILE
71 PRO
72 ARG
79 VAL
80 ALA
81 LEU
82 ILE
83 PRO
84 TYR
85 SER
86 ASP
87 GLN
88 ARG
89 LEU
90 ARG
91 PRO
92 ARG


STRUCTURAL VALIDATION CONTROL
=============================

Residue pair tested:

THR54(A) OG1 → THR54(B) OG1

Measured distance:

40.440 Å

Interpretation:

The same residue number in two chains does not necessarily indicate
structural interaction. Three-dimensional coordinates determine
proximity between atoms.
