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
Due to limited computational resources, a small portion of the dataset has been used for our experiment. Here, we have taken 10,000 training data, 1000 validation data, and 1000 testing data from the CNN/Dailymail dataset. This study utilized Version 3.0.0 of the dataset, which is suitable for training models for both abstractive and extractive summarization tasks. We have also taken 5000 training data, 625 validation data, and 625 testing data from the SAMSum dataset.

# Implementation Details
For fine-tuning the BART, PEGASUS, and ProphetNet, we take the pre-trained _facebook/bart-large-cnn_ model, 
_google/pegasus-cnn_dailymail_ model, and _microsoft/prophetnet-large-uncased_ model from
the hugging face website. For the SEASON model, we fine-tune the pre-trained _facebook/bart-large-cnn_ model. In
the process of preparing the training data, we introduce a unique token before starting every
sentence and computing its representation. Additionally, we limit the length of each
input sequence in the CNN/Dailymail and SAMsum datasets to 1024 and 512 tokens, respectively,
including special tokens. To maintain the essence of the reference summaries
in both datasets, we shorten them to 128 tokens, ensuring that over 99% of the summaries
remain intact. For measuring salience, we experiment with using ROUGE-L F1. During
inference, we utilize predicted soft estimation to allocate expected salience, employing a
temperature of 0.5 to sharpen the probability of salience degree. Our approach for inference
involves using beam search, where the beam width is set to 5, applying a length penalty set to
1.5, and implementing 3-gram blocking. We have conducted training for each of the models
(SEASON, BART, PEGASUS, and ProphetNet) throughout 10 epochs, employing a portion
of the CNN/Dailymail and SAMsum datasets.
