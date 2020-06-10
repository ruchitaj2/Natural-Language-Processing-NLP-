# Natural-Language-Processing-NLP-

## 1.0 Introduction 
The intent of this project is to generate text summaries from receiving a pdf and output the summary in a readable method.  
Many documents, reports, and books are filled with filler words or long contextual expressions dragging a reports to a never ending length.
With current technology and breakthroughs in Natural Language Processing (NLP) and Natural Language Understanding (NLU), it is now possible to summarize many reports at once, or just one report at a time.  

 In most professions, reports are exported or generated as a pdf and stored, with limited knowledge and understanding centralized to the intended audience only. Technical professions generate reports rapidly and the text is often overlooked for diagrams or charts.  
One such professional domain where this happens is in the area of cybersecurity.  The amount of information in cyber security reports is often large and cumbersome to read. 
Thus, I will adapt three pre-built summarization techniques as outlined by github user @theamrzaki, @KaiQiangSong, and SummaNLP (textrank) to identify with tool enables more insight into the document knowledge.  

The illustration above (pg. 1)  is a blueprint for the process and output this report describes.    

## 1.2 Deep Learning NLP 
 Many deep learning techniques are pushing the limit of NLP and NLU forward.  The emergence of OpenAI3 and adaptation of using Natural Language Processing to predict new text or words and generate realistic text is causing trouble in the political arena. Some of the concepts used in NLP deep learning are described below and more through work is currently undergoing for applying deep learning techniques to NLP (Nallapati et al., 2016; Paulus et al., 2017).  To develop a better understanding of the concepts, the thesis presented by (Sanjabi, 2018) and (Song et al., 2019) supported the concepts written below
 
### 1.2.1 Seq2Seq
Seq2Seq or Sequence-to-Sequence is a deep learning technique that processes an input sequence into an output with a tag and attention value to predict a future sequence from a previous sequence using two recurrent neural networks. Seq2Seq relies on an encoder - decoder architecture in order to accurately predict a future sequence. One of the more common applications of this model can be observed in Google Translate where the Seq2Seq is ran on a sequence of one language while predicting that sequence’s resulting translation

### 1.2.2 Encoder - Decoder Architecture

Within recurrent neural networks, the encoder-decoder architecture operates as the fundamental method for neural machine translations. Using the encoder-decoder method allows the model to be trained directly on the input sequence text and predicted sequence text, regardless of varying text length. The encoder-decoder method is used under the assumption that input data can be condensed into a fixed-length vector. A high level process for the encoderdecoder model is described below: 
 
1) The inputted sequence of text is processed element by element in the order that the text is indexed. While the text is being processed, hidden states are created carrying the appropriate weight for each element. The final hidden state produced is called the encoder vector and contains the information necessary for the decoder to make an accurate prediction. This step is classified as the ‘Encoder’. 
 
2) After the ‘Encoder’ phase, the resulting encoder vector is analyzed and a predicted output for each element is generated. While being analyzed, recurrent units borrow the hidden state from the previous unit, resulting in the recurrent unit’s output and it’s own hidden state. At this point the Softmax function is used to create a probability vector that determines the final predicted output

### 1.2.3 Attention Mechanism

The Attention Mechanism is the component of the decoder used to generate a context vector for each output of the input sequence. Essentially the Attention Mechanism is the method by which the output sequence is mapped to the important and relevant words from the input sequence while increasing the weight of the important words to strengthen the accuracy of the prediction output. The Attention Mechanism is operated by the underlying principle that there are two types of attention; additive and multiplicative attention. These varying types of attention differ in the calculations required to generate an alignment score and at what point attention is instituted within the decoder. 

### 1.2.4 Beam Search

Beam Search is the process by which decoding is able to identify the output sequence having the highest probability of occurrence. At the end of the decoding process, there are multiple varying output sequences containing vocabulary that is deemed likely to occur. These candidate sequences are differentiated by their respective likelihoods. In order to isolate the candidate sequence with the highest likelihood, beam search is implemented, sifting through the candidate sequences until the maximum conditional probability is identified through combinations of random states. Typically the larger the beam search width, the more accurate the final identified sequence will be. 

### 1.2.5 Text Summarization 

The concept of text summarization is one that is fairly simple to grasp. Given a large body of text, a technique is implemented that allows the text to be reduced in length while still maintaining the overarching content/message of the original text. Within text summarization, there are two schools of thought to produce the most accurate and effective summaries; extractive and abstractive text summarization.  
 
Extractive Summarization parses through a body of text, assigning weights to individual words and sentences in order to identify the most relevant/important sections of text. Once the most important sequences of text have been classified, they are removed and concatenated with other text from the original corpus that has also been deemed important. While extractive definition is adept at isolating such important portions of a text, the final summary is simply a combination of those portions based on importance and therefore does not read fluidly to human audiences.  
 
On the other hand, Abstractive Summarization paraphrases the original body of text, creating a unique summary that theoretically is easier for humans to read. Abstractive Summarization methods require the algorithms to be able to identify the text language, the grammar of the text, the context of the text, and be able to produce unique sentences to convey the prior texts meaning.

### 1.2.6 Multilayer Bi-directional LSTM/GRU 

GRU or Gated Recurrent Unit is used to resolve the issues surrounding back propagation, specifically that the gradient used to calculate the weights for a neural net become too small to change the weights during each iteration. This increasingly small gradient issue is known as the vanishing gradient problem. Using specific gates, update and reset gates, which are two vectors that identify the relevant information to be progressed to the output.  LSTM or long short-term memory is a type of recurrent neural network architecture that works to resolve the vanishing gradient problem. LSTM is able to mitigate this issue by maintaining gradients from previous iterations when deemed relevant while selectively “forgetting” those that are irrelevant

### 1.2.7 Policy Gradient

Typically policy gradient is a method that is used to approach reinforced learning problems. In order to understand policy gradient one must first understand the two types of policies; deterministic or stochastic. Deterministic policies are focused on the exact steps taken to determine the output (no uncertainty) while stochastic policy examines the probability of each step taken and the potential for other steps to be taken at that time (uncertainty). Using gradient policy one is able to optimize the policies with respect to the output through the gradient descent method.

## 1.3 Other Methods 

### 1.3.1 Automatic Summarization (TextRank) 

Automatic Summarization is very similar to that of DeepLearning text summarization in that it is the method of reducing a large body of text into a shorter concise form while maintaining the message of the original text. However the defining difference between the two is that automatic summarization is done using a computer program. An example of an automatic text summarizer is TextRank, below is the process for its unsupervised text summarization technique.  
 
 
