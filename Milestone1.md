# HBB Variant Pathogenicity Prediction in Sickle Cell Disease
### Project Proposal – Milestone 1

**Student Names:** Kantemir Tkhamokov, Zeynep Aykol

**Course:** ENS210 - Computational Biology

**Date:** 28.10.2026

**Project Option:** Option 1 – Rare Genetic Diseases

**Topic:** Sickle Cell Disease (SCD) – HBB gene

---

## 1. Project Objective

The objective of this project is to develop and evaluate a reproducible computational workflow for distinguishing likely pathogenic from likely benign variants in the HBB gene associated with sickle cell disease (SCD). We will use clinically classified variants from ClinVar, population allele frequencies from gnomAD, and biological annotations. We will compare a simple rule-based baseline with selected existing prediction tools or a basic machine-learning classifier, depending on dataset size and quality. The final output will be a documented dataset, a reproducible analysis workflow, and an evaluation of prediction performance.

---

## 2. Background

Sickle cell disease is an inherited blood disorder associated with abnormal hemoglobin, which can cause red blood cells to become sickle-shaped. This can lead to anemia, painful vaso-occlusive episodes, and other complications. The HBB gene encodes the beta-globin subunit of hemoglobin. A well-known disease-associated variant is HBB c.20A>T, which produces the HbS variant (p.Glu7Val using precursor-protein numbering, commonly called Glu6Val in mature beta-globin). Sickle cell disease is typically inherited in an autosomal-recessive pattern.

Computational prediction of variant pathogenicity is challenging because clinical classifications can be uncertain or conflicting, datasets may contain unequal numbers of pathogenic and benign variants, and population frequency alone cannot establish whether a variant causes disease. Duplicate records and overlap between training and test data can also lead to misleading performance estimates. Therefore, careful data filtering, consistent variant annotation, and appropriate evaluation metrics are important.

---

## 3. Data Sources

| Source | What I will get from it |
|---|---|
| ClinVar | HBB variant records, clinical significance classifications, review status, and supporting evidence. We will initially select pathogenic/likely pathogenic and benign/likely benign variants. |
| gnomAD | Population allele frequencies for available HBB variants, used as candidate features and to describe variant frequency. |
| OMIM | Background information about sickle cell disease, inheritance, HBB, and the gene–disease relationship. |
| Ensembl Variant Effect Predictor (VEP) | Variant consequence and transcript annotations, if needed and available. |
| SIFT, PolyPhen-2, CADD, or REVEL | Available in-silico prediction scores for comparison or as candidate features, depending on data availability. |

---

## 4. Methodology / Approach

**Step 1:** Develop a workflow to classify HBB variants as likely pathogenic or likely benign and compare a baseline with selected computational prediction methods.

**Step 2:** Retrieve HBB variant records and clinical classifications from ClinVar, supplemented with population frequencies from gnomAD and relevant biological annotations.

**Step 3:** Standardize variant descriptions, check for duplicate records, and document inclusion and exclusion criteria. Keep variants with uncertain or conflicting classifications separate from the initial binary dataset.

**Step 4:** Construct a labelled dataset with available features, including variant consequences, amino-acid changes, population allele frequencies, and in-silico prediction scores.

**Step 5:** Establish a simple rule-based baseline and compare it with selected existing prediction tools or a basic machine-learning classifier, depending on dataset size and label quality.

**Step 6:** Evaluate performance using accuracy, sensitivity, specificity, and Matthews correlation coefficient (MCC). Where applicable, use separate training and test sets and check for duplicate records and potential data leakage.

**Step 7:** Present results in tables and figures, compare the methods, and discuss limitations such as class imbalance, uncertain clinical labels, and the limits of computational predictions.

By the end of the project, we expect to produce a reproducible HBB variant-analysis workflow, a documented dataset, and an evaluation of prediction performance. The results will be computational research outputs, not clinical diagnoses.

---

## 5. AI Tool Disclosure

ChatGPT was used to help organize and edit this proposal. The students will verify scientific claims and data sources, review and test any AI-assisted code, and ensure that they can explain all methods and results in the submitted work.

---

## References

1. National Center for Biotechnology Information. (n.d.). *ClinVar*. https://www.ncbi.nlm.nih.gov/clinvar/
2. gnomAD. (n.d.). *Genome Aggregation Database*. https://gnomad.broadinstitute.org/
3. Online Mendelian Inheritance in Man. (n.d.). *OMIM*. https://omim.org/
4. Ensembl. (n.d.). *Variant Effect Predictor*. https://www.ensembl.org/info/docs/tools/vep/index.html
