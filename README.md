# (Partically) Annotated Bibliography for Question Answering and Reading Comprehension Datasets
Ansong Ni

#### Note: ####
Since there are too many datasets are in the format of question answering, here we explictly exclude the datasets that are of the following format/purpose, please refer to the specified links for those topics(if any):
* Commonsense reasoning: https://github.com/michiyasunaga/nlp_bibs/blob/master/commonsense.md (by Michihiro Yasunaga)
* Visual question answering (VQA)
* Table-based question answering (mostly fully- or weakly-supervised semantic parsing)

## Short context QA (no retrieval needed)
[**SQuAD: 100,000+ Questions for Machine Comprehension of Text**](https://arxiv.org/abs/1606.05250)[[leaderboard](https://rajpurkar.github.io/SQuAD-explorer/)]

Pranav Rajpurkar, Jian Zhang, Konstantin Lopyrev, Percy Liang (EMNLP'16)

This paper presents the first large-scale (100K+) reading comprehension dataset, created by crowd-sourcing. The context are curated paragraphs from Wikipedia articles. From the 536 selected Wikipedia articles, a total number of 23,215 number of paragraphs are chosen to be the context where the crowd-source workers will be generating questions about. The answer of the question are all spans in the context, thus rendering this QA problem extractive in nature.

[**Know What You Don't Know: Unanswerable Questions for SQuAD**](https://arxiv.org/abs/1806.03822)[[leaderboard](https://rajpurkar.github.io/SQuAD-explorer/)]

Pranav Rajpurkar, Robin Jia, Percy Liang (ACL'18)

In this paper, an important aspect of the reading comprehension problem is studied: the unanswerable questions. The authors found that extractive reading comprehension systems tend to produce unreliable answers when the correct answering is not a span of the context. For the purpose of building more robust machine reading comprehension systems, they propose to adversarially create additional 50K+ unanswerable questions to augment the SQuAD dataset.

[**DROP: A Reading Comprehension Benchmark Requiring Discrete Reasoning Over Paragraphs**](https://arxiv.org/abs/1903.00161)[[project page](https://allennlp.org/drop)]

Dheeru Dua, Yizhong Wang, Pradeep Dasigi, Gabriel Stanovsky, Sameer Singh, Matt Gardner (NAACL'19)

This paper introduces the first reading comprehension dataset that requires numerical reasoning (e.g., addition/subtraction, count, sorting, etc) to answer the questions. It consists of 96K questions written by crowdsource workers based on Wikipedia paragraphs. Those discrete operations demands a much higher level of comprehensive understanding of the textual data than previous datasets. 

[**Quoref: A Reading Comprehension Dataset with Questions Requiring Coreferential Reasoning**](https://arxiv.org/abs/1908.05803)[[project page](https://allennlp.org/quoref)]

Pradeep Dasigi, Nelson F. Liu, Ana Marasović, Noah A. Smith, Matt Gardner (EMNLP'19)

[**Looking Beyond the Surface: A Challenge Set for Reading Comprehension over Multiple Sentences**](https://cogcomp.seas.upenn.edu/papers/2018-MultiRC-NAACL.pdf)[[project page](https://cogcomp.seas.upenn.edu/multirc/)]

Daniel Khashabi, Snigdha Chaturvedi, Michael Roth, Shyam Upadhyay, Dan Roth (NAACL'18)

***
## Document-level or multi-document QA (retrival needed)

[**The NarrativeQA Reading Comprehension Challenge**](https://www.aclweb.org/anthology/Q18-1021/)[[project page](https://deepmind.com/research/open-source/narrativeqa)]

Tomáš Kočiský, Jonathan Schwarz, Phil Blunsom, Chris Dyer, Karl Moritz Hermann, Gábor Melis, Edward Grefenstette (TACL'18)


[**Constructing Datasets for Multi-hop Reading Comprehension Across Documents**](https://www.aclweb.org/anthology/Q18-1021/)[[project page](http://qangaroo.cs.ucl.ac.uk/)]

Johannes Welbl, Pontus Stenetorp, Sebastian Riedel (TACL'18)

[**HotpotQA: A Dataset for Diverse, Explainable Multi-hop Question Answering**](https://arxiv.org/abs/1809.09600)[[project page](https://hotpotqa.github.io/)]

Zhilin Yang, Peng Qi, Saizheng Zhang, Yoshua Bengio, William W. Cohen, Ruslan Salakhutdinov, Christopher D. Manning (EMNLP'18)

This work characterizes the problem of multi-hop reasoning. This is a dataset consisting of 113K QA examples requiring context from two distinct paragraphs from Wikipedia to be able to answer the questions. The annotations also contain the sentences in the paragraphs that are supporting facts for deriving at the correct answer. This dataset brings challenges to both question answering systems as well as information retrieval systems on free-form textual data. 

[**IIRC: A Dataset of Incomplete Information Reading Comprehension Questions**](https://arxiv.org/abs/2011.07127)[[project page](https://hotpotqa.github.io/)]

James Ferguson, Matt Gardner, Hannaneh Hajishirzi, Tushar Khot, Pradeep Dasigi (EMNLP'20)

[**Natural Questions: a Benchmark for Question Answering Research**](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/1f7b46b5378d757553d3e92ead36bda2e4254244.pdf)[[project page](https://ai.google.com/research/NaturalQuestions)]

Tom Kwiatkowski, Jennimaria Palomaki, Olivia Redfield, Michael Collins, Ankur Parikh, Chris Alberti, Danielle Epstein, Illia Polosukhin, Matthew Kelcey, Jacob Devlin, Kenton Lee, Kristina N. Toutanova, Llion Jones, Ming-Wei Chang, Andrew Dai, Jakob Uszkoreit, Quoc Le, Slav Petrov (TACL'19)

[**TyDi QA: A Benchmark for Information-Seeking Question Answering in Typologically Diverse Languages**](https://arxiv.org/abs/2003.05002)[[project page](https://ai.google.com/research/tydiqa)]

Jonathan H. Clark, Eunsol Choi, Michael Collins, Dan Garrette, Tom Kwiatkowski, Vitaly Nikolaev, Jennimaria Palomaki (TACL'20)

[**TriviaQA: A Large Scale Distantly Supervised Challenge Dataset for Reading Comprehension**](https://arxiv.org/abs/1705.03551)[[project page](https://nlp.cs.washington.edu/triviaqa/)]

Mandar Joshi, Eunsol Choi, Daniel S. Weld, Luke Zettlemoyer (ACL'17)

## Conversational QA

[**CoQA: A Conversational Question Answering Challenge**](https://arxiv.org/abs/1808.07042)[[project page](https://stanfordnlp.github.io/coqa/)]

Siva Reddy, Danqi Chen, Christopher D. Manning (TACL'19)

[**QuAC : Question Answering in Context**](https://arxiv.org/abs/1808.07036)[[project page](https://quac.ai/)]

Eunsol Choi, He He, Mohit Iyyer, Mark Yatskar, Wen-tau Yih, Yejin Choi, Percy Liang, Luke Zettlemoyer (EMNLP'18)

[**Interpretation of Natural Language Rules in Conversational Machine Reading**](https://arxiv.org/abs/1809.01494)[[project page](https://sharc-data.github.io/)]

Marzieh Saeidi, Max Bartolo, Patrick Lewis, Sameer Singh, Tim Rocktäschel, Mike Sheldon, Guillaume Bouchard, Sebastian Riedel (EMNLP'18)

## QA on dialogues

[**FriendsQA: Open-Domain Question Answering on TV Show Transcripts**](https://www.aclweb.org/anthology/W19-5923/)[[project page](https://github.com/emorynlp/FriendsQA)]

Zhengzhe Yang, Jinho D. Choi (SIGDial'19)

[**DREAM: A Challenge Dataset and Models for Dialogue-Based Reading Comprehension**](https://arxiv.org/abs/1902.00164)

Kai Sun, Dian Yu, Jianshu Chen, Dong Yu, Yejin Choi, Claire Cardie (TACL'19)
