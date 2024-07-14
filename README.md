
## Text Analysis Project

This project performs a comprehensive text analysis using Natural Language Processing (NLP) techniques. The analysis includes calculating various text metrics such as sentiment scores, readability indices, and more. The project is implemented in a Jupyter Notebook and leverages Python libraries like `nltk`, `textblob`, and `pyphen`.

### Files Included
- **code.ipynb**: The Jupyter Notebook containing the code for text analysis.

### Dependencies
To run this notebook, you need to have the following Python libraries installed:
- `nltk`
- `textblob`
- `pyphen`
- `pandas`

You can install these dependencies using pip:
```sh
pip install nltk textblob pyphen pandas
```

### Usage
1. **Import Necessary Libraries**: The first step is to import all the required libraries.
   ```python
   import nltk
   from textblob import TextBlob
   import pyphen
   import pandas as pd
   ```

2. **Download NLTK Data**: Ensure the necessary NLTK data packages are downloaded.
   ```python
   nltk.download('punkt')
   ```

3. **Define Helper Functions**: Several helper functions are defined to assist with text analysis.
   - `count_syllables(word)`: Counts the number of syllables in a word.
   - `analyze_text(text)`: Analyzes the text and returns a dictionary of various text metrics.

4. **Analyze Text**: Call the `analyze_text` function with the text you want to analyze.
   ```python
   text = "Your text here"
   analysis_results = analyze_text(text)
   ```

5. **Save Results to CSV**: The results of the analysis can be saved to a CSV file.
   ```python
   df = pd.DataFrame([analysis_results])
   df.to_csv('analysis_results.csv', index=False)
   ```

### Metrics Calculated
- **Positive Score**: Number of positive words.
- **Negative Score**: Number of negative words.
- **Polarity Score**: Overall sentiment polarity of the text.
- **Subjectivity Score**: Overall subjectivity of the text.
- **Avg Sentence Length**: Average length of sentences.
- **Percentage of Complex Words**: Percentage of words with more than two syllables.
- **Fog Index**: Readability index based on sentence length and complex words.
- **Avg Number of Words Per Sentence**: Average number of words per sentence.
- **Complex Word Count**: Total count of complex words.
- **Word Count**: Total word count.
- **Syllables per Word**: Average number of syllables per word.
- **Personal Pronouns**: Count of personal pronouns.
- **Avg Word Length**: Average word length.

### Example
```python
text = "This is an example sentence for text analysis."
analysis_results = analyze_text(text)
print(analysis_results)
```

### Downloading Results
At the end of the notebook, there is a cell to download the `analysis_results.csv` file.

```python
from google.colab import files
files.download('analysis_results.csv')
```

### Conclusion
This project provides a detailed analysis of text using various NLP metrics. It can be extended further to include more advanced analysis techniques or integrated into a larger application for real-time text analysis.
