# NLTK Commands and Functions Table

| **Function/Command/Expression** | **Description** |
|--------------------------------|---------------|
| `from nltk.book import *` | Loads sample texts and predefined sentence variables from NLTK. |
| `sents()` | Lists available texts and sentence samples. |
| `text1` | Refers to 'Moby Dick' text loaded from NLTK. |
| `sent1` | Preloaded list containing `['Call', 'me', 'Ishmael', '.']`. |
| `len(text1)` | Counts total words (tokens) in `text1`. |
| `set(text1)` | Extracts unique words (types) from `text1`. |
| `len(set(text1))` | Counts the number of unique words in `text1`. |
| `sorted(set(text1))` | Sorts unique words alphabetically. |
| `text1.count('whale')` | Counts occurrences of the word 'whale' in `text1`. |
| `text1.concordance('monstrous')` | Displays words surrounding 'monstrous' in `text1`. |
| `text1.similar('monstrous')` | Finds words used in similar contexts as 'monstrous' in `text1`. |
| `text2.common_contexts(['monstrous', 'very'])` | Finds shared contexts for 'monstrous' and 'very' in `text2`. |
| `text4.dispersion_plot(['citizens', 'democracy'])` | Plots occurrences of words across `text4`. |
| `text3.generate()` | Generates random text in the style of `text3`. |
| `def lexical_diversity(text): return len(set(text)) / len(text)` | Defines a function to compute lexical diversity. |
| `def percentage(count, total): return 100 * count / total` | Defines a function to compute percentage. |
| `lexical_diversity(text3)` | Computes lexical diversity for `text3`. |
| `percentage(text4.count('a'), len(text4))` | Finds the percentage of 'a' in `text4`. |
| `FreqDist(text1)` | Creates a frequency distribution of words in `text1`. |
| `fdist1.most_common(50)` | Gets the 50 most common words in `fdist1`. |
| `fdist1.plot(50, cumulative=True)` | Plots the cumulative frequency of the 50 most common words. |
| `fdist1.hapaxes()` | Finds words that appear only once in `text1`. |
| `[w for w in set(text1) if len(w) > 15]` | Finds words in `text1` longer than 15 characters. |
| `sorted(w for w in set(text5) if len(w) > 7 and fdist5[w] > 7)` | Finds long words (7+ characters) appearing more than 7 times in `text5`. |
| `fdist.most_common()` | Displays the most common word lengths and their counts. |
| `fdist.max()` | Finds the most frequent word length in the text. |
| `fdist.freq(X)` | Finds the percentage of words with length X. |
| `fdist.plot(15, cumulative=False)` | Plots individual frequencies of word lengths (bar chart). |
| `fdist.plot(15, cumulative=True)` | Plots cumulative frequency of word lengths (rising curve). |
| `if len(word) < 5:` | Conditional check: Runs block only if word length is less than 5. |
| `for word in sent1:` | Loops through each word in `sent1`. |
| `if word.endswith('l'):` | Checks if a word ends with 'l'. |
| `sorted(w for w in set(text2) if 'cie' in w or 'cei' in w)` | Finds words in `text2` containing 'cie' or 'cei'. |
| `not s.islower()` | Checks if a word is **not** fully lowercase. |
| `s.isupper()` | Checks if all characters are uppercase. |
| `s.istitle()` | Checks if the first letter is uppercase, rest lowercase (title case). |
| `len(set(word.lower() for word in text1))` | Finds unique lowercase words in `text1` (removes case sensitivity). |
| `len(word.lower() for word in set(text1))` | Creates a generator that applies `.lower()`, but does not compute unique words properly. |
| `len(set(word.lower() for word in set(text1)))` | Corrected version that finds unique words after removing case differences. |