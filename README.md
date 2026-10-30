Computational Classification of Tantrayuktis in Sanskrit Texts
Overview
This repository contains the source datasets and code for a
computational study of sentence-level tantrayukti classification in
two Sanskrit philosophical texts: the Tarka-saṅgraha of Annaṃbhaṭṭa
and the Vedāntasāra of Sadānanda.
The study investigates whether traditional Sanskrit discourse functions
can be classified computationally at the sentence level, compares
word-level and character-level TF-IDF representations, and examines the
transfer of the approach to a second annotated text.
Repository contents
---
File                                Description
---
`Tarka_sangraha_moola.xlsx`         Source spreadsheet containing the
Tarka-saṅgraha text and
associated conceptual and
annotation material.
`Vedanta-saara (1).xlsx`            Spreadsheet containing the
Vedāntasāra text and material
used for the cross-text pilot
evaluation.
`tantrayukti_code.zip`              Archive containing the code used
for data processing and/or
computational experiments. Extract
this archive to access the scripts
and notebooks.
Research focus
The experiments address three questions:
Can sentence-level tantrayukti labels in the Tarka-saṅgraha be
classified using computational methods?
Do character-level TF-IDF features perform better than word-level
TF-IDF features for this Sanskrit classification task?
Do the patterns observed in the Tarka-saṅgraha experiment
generalise to a second annotated text, the Vedāntasāra?
Character n-grams are examined because Sanskrit word-level processing
can be affected by morphological variation, sandhi, and compound
formation, which may complicate tokenisation and the identification of
word boundaries.
Dataset and annotation
The Tarka-saṅgraha source workbook contains multiple sheets with
textual, conceptual, and tantrayukti-related material. The research
dataset was prepared by selecting and organising sentence-level
instances for classification.
The annotation reference set consists of consolidated labels refined
iteratively by three researchers. Each sentence has one consensus label
in the final reference set. Since the experiment uses this consolidated
reference set, inter-annotator agreement statistics are not reported.
The descriptive category distribution and the predictive evaluation use
different label sets:
Descriptive analysis: 13 tantrayukti categories.
Predictive evaluation: 11 categories, after excluding two
categories represented by only one instance each.
The Vedāntasāra workbook supports a pilot cross-text evaluation using
the labels shared by the two texts. The reported pilot uses nine shared
labels.
Experimental approach
The classification experiments compare:
A majority-class baseline.
Word-level TF-IDF features with a Linear Support Vector Classifier
(LinearSVC).
Character-level TF-IDF features with a LinearSVC.
The evaluation uses:
A stratified holdout split.
Repeated stratified cross-validation.
A comparison of word-level and character-level feature
representations.
The cross-text pilot investigates whether the representations learned or
selected for the Tarka-saṅgraha task transfer effectively to the
Vedāntasāra. The pilot results should be interpreted separately from
the primary within-text classification results.
Reported findings
In the primary Tarka-saṅgraha experiment, character-level TF-IDF
outperformed word-level TF-IDF under both evaluation protocols. However,
the difference in the stratified holdout evaluation was not
statistically significant.
In the pilot cross-text evaluation involving the nine shared labels,
neither representation transferred strongly to the Vedāntasāra, and
the character-level advantage observed in the primary experiment did not
persist.
These findings suggest that character-level features are useful for the
within-text classification task examined here, but that performance on
one Sanskrit text does not necessarily transfer to another text without
further investigation.
How to access the materials
Download or clone this repository.
Open the two `.xlsx` workbooks using Microsoft Excel, LibreOffice
Calc, or a compatible spreadsheet application.
Extract `tantrayukti_code.zip`.
Inspect the extracted files for the relevant scripts or notebooks
and their execution order.
Run the code in the environment and with the dependencies specified
by the code files.
Reproducibility note: The archive contents and dependency versions
should be documented alongside the code. Before reproducing the reported
results, verify that the scripts use the same curated datasets, label
mappings, train/test split, random seeds, and cross-validation settings
as the study.
Scope and limitations
This repository supports an exploratory computational study of
tantrayukti classification. The annotation reference set is a
consolidated consensus dataset rather than a set of independently
retained annotator outputs; therefore, inter-annotator agreement cannot
be calculated from the reported annotations. The pilot cross-text
evaluation is limited to the nine labels shared by the two texts.
Further work should examine additional Sanskrit treatises, annotation
procedures, and cross-text evaluation settings.
Citation
If you use these datasets or code, please cite the associated research
paper. Add the complete bibliographic reference here once the paper's
publication details are available.
Data and code status
The repository includes the source workbooks and a compressed code
archive. Please consult the associated paper for the precise
experimental design, dataset preparation decisions, evaluation protocol,
and results.
