# Results

The chart below shows the Original Text and the summarized text from each model.  The text used for this example is the book Pride and Prejudice obtained from the gutenberg text.  

The entire book was converted into a .pdf, then passed into the pdf to text filter.  After it was passed into the BERT summarizer (output) shown below.  The original text (.pdf) was summarized before to reduce the length of tokenized sentences to pass into the other three models.  Inspecting the results of each model, the TextRank automatic summarization model appears to return the most coherent text.  This is true because the algorithm within the SummaNLP API inspects the text and selects the highest weighted sentences to return.  

The summarization also reads well, but lacks cohesion.  This summarization technique is the best performing among the three.   The point-generated deep summary model performs abstractive summarization.  It reads in 5 sentences at a time and summarizes them with new generated text.  The text lacks both cohesion and coherence and therefore does not act as a good summarizer for the input text.  The final summarizer generates smaller sentences for each sentence in the original text.  The model does actually have coherence as it summarizes the original text covers but is not very cohesive.  Ultimately, the best results are generated from the BERT Summarizer and the Automatic Summarization techniques like TextRan

