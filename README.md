# B211_Assignment-9

Purpose:
- Project implements NLP techniques to analyze unstructured text data.
- Aims to identify the top tokens, common phrases, named entities, and potential authorship matches between four different text files.

Class Design:
- Uses a 'TextAnalyzer' class to encapsulate all NLP operations
- _init_: Loads the file.
- process_text: Performs cleaning, tokenization, stop word removal, and lemmatization.
- get_top_tokens: Returns FreqDist of tokens.
- extract_named_entities: Uses SpaCy for NER.
- get_ngrams: Generates n-grams (3-grams) for style analysis.

Limitations:
- NER Accuracy: SpaCy's 'en_core_web_sm' is fast, but might miss entities compared to larger models.
- Lemmatization Constraints: WordNet lemmatizer relies on POS tagging, which can misinterpret words without context.
- Authorship Accuracy: N-gram analysis is a soimple stylometric method; actual authorship analysis would require advanced machine learning models.
