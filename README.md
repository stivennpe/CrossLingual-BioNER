# CrossLingual-BioNER
Data Augmentation and Transfer Learning for Cross-lingual Named Entity Recognition in the Biomedical Domain

The Folders contain the final datasets to train a Named Entity Recognition system using the CRAFT dataset. It includes the following entities:
- Protein
- Chemical
- Taxon
- Gene
- Cell
- Sequence

These datasets are the result of a project where back-translation and data augmentation were used to create syntethic versions of the original CRAFT dataset as follows:

1. ``Original`` folder:

  It contains the original CRAFT dataset as found in the repository: [MLT-Bioinformatics2016](https://github.com/cambridgeltl/MTL-Bioinformatics-2016/tree/master/data/CRAFT-IOB).

  
2. ``SpanishTranslated`` folder:

  Contains the original CRAFT dataset translated to Spanish using neural Google Translate.
  
3. ``EN+SP`` folder:

  Contains the original CRAFT dataset plus the Spanish (MT translated) concatenated in a single dataset. 
  
4. ``Original+Augmented`` folder:

  Contains the original CRAFT dataset plus an augmented version of the same. It was created using entity replacement (follow Liu et al. (2020)) with entities of the same category extracted from the original official ontologies.
  
5. ``Original+ES+Augmented`` folder:

  Contains a concatenated version of the original CRAFT dataset plus the augmented version plus the Spanish version. This dataset aims to be a resource for cross-lingual NER in the biomedical domain in English and Spanish.
  
All datasets use the IOB annotation scheme: B- beginning, I- inside and O for tokens not corresponding to any tag, e.g., B-Protein, and I-Taxon.
