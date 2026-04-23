# B211_Assignment-9

Purpose:
- Project implements NLP techniques to analyze unstructured text data.
- Aims to identify the top tokens, common phrases, named entities, and potential authorship matches between four different text files.

# B211_Assignment-9

Purpose:
- Project implements NLP techniques to analyze unstructured text data.
- Aims to identify the top tokens, common phrases, named entities, and potential authorship matches between four different text files.

Class Design:
TextAnalyzer: A container class that isolates the data and processing for a single file.
_load_text: Ensures the file is read in a standard UTF-8 format.
extract_entities: Uses spaCy’s pre-trained transformer models to identify real-world objects.

Implementation Details:
- N-Grams: Chosen for authorship because sequences of 3 words (trigrams) act like a stylistic "fingerprint" better than single words.
- Lemmatization: Preferred over stemming for subject analysis because it keeps words in a dictionary-recognizable format (e.g., "running" becomes "run").

Limitations:
- Size: doc = nlp(self.text[:100000]) limits analysis to the first 100k characters to prevent memory crashes.
- Accuracy: Authorship is based on overlap, which is less accurate for very short texts.
