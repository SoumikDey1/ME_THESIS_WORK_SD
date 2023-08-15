# ME_THESIS_WORK_SD
Abstractive text summarization entails producing summaries that encompass the essential
concepts present in the original text. Unlike extractive summarization, abstractive summarization
can include new expressions and sentences absent from the original text. This thesis  entitled **“Analysis of Abstractive Summarization Using Salience Allocation”** presents a comprehensive analysis of abstractive summarization using the salience allocation
technique. The study incorporates a novel summarization model called SEASON. SEASON
uses the distribution of anticipating relevance to facilitate abstractive text summarization,
effectively responding to the content with various levels of abstraction.

This thesis work aims to assess SEASON’s performance in guiding effective abstractive
summarization across diverse articles and conversations, comparing it with the latest models
like BART, PEGASUS, and ProphetNet fine-tuned for text summarization tasks. The focus
is on measuring the quality and effectiveness of the generated summaries, considering their
ability to capture essential information and produce concise and coherent summaries.

The CNN/Dailymail and SAMSum datasets are used to conduct this study. In the study,
the performance of these models in text and dialogue summarization is assessed using a range of evaluation
metrics. These metrics include ROUGE, METEOR, MoverScore, and BERTScore.
Analyzing the evaluation results enables a comprehensive comparison of the strengths and
weaknesses exhibited by each model.

This study sheds light on SEASON’s potential as a novel summarization model. It provides
awareness of the benefits and restrictions of different models in salience allocation. The
findings contribute to advancing the field of abstractive summarization and provide valuable
guidance for future research endeavors.

# Dataset Used
Due to limited computational resources, a small portion of the dataset has been used for our experiment. Here, we have taken 10,000 training data, 1000 validation data, and 1000 testing data from the CNN/Dailymail dataset. In this study, Version 3.0.0 of the dataset was utilized, which is suitable for training models for both abstractive and extractive summarization tasks. We have also taken 5000 training data, 625 validation data, and 625 testing data from the SAMSum dataset.
