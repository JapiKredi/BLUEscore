# BLUEscore

BLEU (Bilingual Evaluation Understudy) is another widely used metric for evaluating the quality of generated text, especially in the context of machine translation. BLEU was originally designed for assessing the quality of machine-translated text by comparing it with one or more reference translations.

The BLEU score is based on the precision of n-grams in the generated text, where n can be 1, 2, 3, or 4 (unigrams, bigrams, trigrams, or quadgrams). BLEU considers not only precision but also penalizes for brevity, encouraging the generated text to have similar length to the reference text.

Here's a simplified explanation of the BLEU calculation:

Precision (BLEU-P): It measures the proportion of n-grams in the generated text that also appear in the reference text.

<img width="759" alt="Screenshot 2024-01-21 at 4 36 38 PM" src="https://github.com/JapiKredi/BLUEscore/assets/88824661/6261ff29-534d-4682-ae99-d1dab1967b23">

Brevity Penalty (BLEU-BP): It penalizes the generated text for being too short compared to the reference text. If the generated text is shorter than the reference text, a penalty is applied.

<img width="765" alt="Screenshot 2024-01-21 at 4 38 12 PM" src="https://github.com/JapiKredi/BLUEscore/assets/88824661/250c9706-6088-47c9-8299-105435751ee9">

BLEU Score (BLEU-S): It combines precision and brevity penalty to get the final BLEU score.

<img width="643" alt="Screenshot 2024-01-21 at 4 39 14 PM" src="https://github.com/JapiKredi/BLUEscore/assets/88824661/1e5c52b2-8368-4d01-8fd3-e8a4d6658c9b">

Now, let's consider a simple example for BLEU-1 (unigram) with a generated text and a reference text:

Generated Text: The quick brown fox jumps over the lazy dog.

Reference Text: A quick brown fox jumps over a lazy dog.

In this case, the unigrams (individual words) that overlap are: "the," "quick," "brown," "fox," "jumps," "over," "the," "lazy," "dog." There are a total of 9 unigrams in the generated text.

Now, let's calculate BLEU-P, BLEU-BP, and BLEU-S:

<img width="481" alt="Screenshot 2024-01-21 at 4 40 47 PM" src="https://github.com/JapiKredi/BLUEscore/assets/88824661/00161fbf-c6df-4cd0-8482-0f52c91432a0">

In this example, the BLEU-1 precision, brevity penalty, and BLEU score are all perfect, indicating a complete overlap between the generated text and the reference text in terms of unigrams, and the lengths of the generated and reference texts are the same.
