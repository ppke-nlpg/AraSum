# AraSum 


This repository contains the **AraSum** corpus which is the first monolingual corpus in the Arabic language for abstractive text summarization. For details of how we created the corpus, please refer to our paper: [**Cross-lingual Fine-tuning for Abstractive Arabic Text Summarization**](https://aclanthology.org/2021.ranlp-1.74/) published in the _Proceedings of the International Conference on Recent Advances in Natural Language Processing (RANLP 2021)_.




We are releasing the **AraSum** corpus which is the first monolingual corpus for abstractive text summarization for the Arabic language. The **AraSum** corpus contains 49604 articles and their corresponding leads.


The source for **AraSum** corpus is the Arabic version of the Deutsche Welle DW news website. The downloaded items address a wide range of topics, not only dealing with politics, sports, or art. This allows the summary database to cover a wide range of topics, making more realistic testing of the capabilities of the summarization models as well as the creation of more robust and less domain-dependent models possible.


AraSum files are in ```.csv``` format one CSV per line each line contains an article TAB lead.

## Citation: 
If you use our corpus, please cite the following paper: 
```
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
