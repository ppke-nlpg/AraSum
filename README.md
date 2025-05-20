# AraSum 


This repository contains **AraSum**, the first large-scale **monolingual Arabic corpus** for **abstractive text summarization**, as well as two newly released datasets for **preference-based fine-tuning**:

- `AraRLHF`: A dataset formatted for Reinforcement Learning from Human Feedback (RLHF)
- `AraDPO`: A dataset formatted for Direct Preference Optimization (DPO)


## 📚 Datasets


### 🔹 AraSum

AraSum is a monolingual Arabic summarization corpus containing **49,604 articles and their corresponding leads**. It was constructed from the **Arabic version of the Deutsche Welle (DW) news website**, covering diverse domains such as politics, sports, and culture. This diversity promotes better generalization in summarization models.

- **Format**: `.csv`
- **Structure**: Each line contains an article and its lead summary, separated by a tab (`\t`)

**Related Publications**  
For more details on the creation and usage of this dataset, please refer to the following papers:

- [**Cross-lingual Fine-tuning for Abstractive Arabic Text Summarization**](https://aclanthology.org/2021.ranlp-1.74/)  
  *Proceedings of the International Conference on Recent Advances in Natural Language Processing (RANLP 2021)*

- [**Fine-tuning and Multilingual Pre-training for Abstractive Summarization Task for the Arabic Language**](https://doi.org/10.33039/ami.2022.11.002)  
  *Annales Mathematicae et Informaticae (2022)*

### 🔹 AraRLHF

A JSON-formatted dataset designed for **training reward models** in Reinforcement Learning from Human Feedback (RLHF) pipelines.
The AraRLHF dataset consists of **1,746 samples**, derived from **manual evaluation results** conducted in our prior research.

This dataset is used to **train a reward model (RM)** that predicts the quality of a generated summary based on human preferences.


- **Format**: `.json`
- **Structure**: Each record includes: An article, its lead summary, a ranking label reflecting human preference, and the evaluator ID (author)
  
### 🔹 AraDPO

A JSON-formatted dataset designed for **Direct Preference Optimization (DPO)**, following the same structure as **AraRLHF**.
The AraDPO dataset is used to fine-tune language models directly using **binary preference pairs**.
To construct AraDPO, each ranked preference entry in AraRLHF was converted into all possible pairwise comparisons. We then applied deduplication to remove redundant or overlapping pairs, resulting in a final set of **2,309 unique preference records**.

This dataset is used to **Fine-tuning language models with DPO**.

- **Format**: `.json`
- **Structure**: Each record includes: article_id, article, chosen (the preferred summary ), and rejected (the dispreferred summary).


## 🔖 Citation

If you use **AraSum**, please cite:

```bibtex
@inproceedings{kahla-etal-2021-cross,
    title = "Cross-lingual Fine-tuning for Abstractive {A}rabic Text Summarization",
    author = "Kahla, Mram  and
      Yang, Zijian Gy{\H{o}}z{\H{o}}  and
      Nov{\'a}k, Attila",
    booktitle = "Proceedings of the International Conference on Recent Advances in Natural Language Processing (RANLP 2021)",
    month = sep,
    year = "2021",
    address = "Held Online",
    publisher = "INCOMA Ltd.",
    url = "https://aclanthology.org/2021.ranlp-1.74",
    pages = "655--663",
}
```

We will release formal citations for AraRLHF and AraDPO soon. Until then, please link to this repository.





