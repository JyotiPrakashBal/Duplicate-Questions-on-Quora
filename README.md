# Duplicate-Questions-on-Quora

<b>Problem Statement : 
<br/> <br/>
</b>
Identify which questions asked on Quora are duplicates of questions that have already been asked. This is a Kaggle Problem. The datasets are available on [Link](https://www.kaggle.com/c/quora-question-pairs)
<br/> <br/>
<b>Data : <br/><br/>
</b>
Train.csv contains 5 columns : qid1, qid2, question1, question2, is_duplicate. Total we have 404290 entries <br/><br/>
<b>Feature Extraction:
<br/> <br/> </b>
<b>len_q1</b>: Length of Question 1 <br/>
<b>len_q2</b>: Length of Question 2 <br/>
<b>len_diff</b>: Difference in length of Question 1 and Question 2 <br/>
<b>len_char_q1</b>: No of characters in Question 1 without spaces <br/>
<b>len_char_q2</b>: No of characters in Question 2 without spaces <br/>
<b>len_word_q1</b>: No of words in Question 1 <br/>
<b>len_word_q2</b>: N of words in Question 2 <br/>
<b>common_words</b>: No of common words in Question 1 and Question 2 <br/>
<b>fuzz_qratio</b>: How much percentage these two strings are similar, measured with edit distance <br/>
<b>fuzz_WRatio</b>: WRatio handles lower and upper cases and some other parameters too. <br/>
<b>fuzz_partial_ratio</b>: score of the best matching lowest length substring.
<br/><b>fuzz_partial_token_set_ratio</b>: partial tokenizer
<br/><b>fuzz_partial_token_sort_ratio</b>: partial tokenizer
<br/><b>fuzz_token_set_ratio</b>: token_set_ratio that takes out the common tokens and then makes fuzz.ratio() pairwise comparisons
<br/><b>fuzz_token_sort_ratio</b>: sorting the tokens in string and then scoring fuzz_ratio. <br/>
<br/>
Got <b>Word Movers Distance</b> with pretrained Google news word vectors.</b>
<br/>
</br>
From Pretrained Google news word vectors got  sent2vec for question1 and question2. With this sent2vec got the distances: <br/>
<b>Cosine distance,Cityblock distance,Canberra distance,Euclidean distance,Minkowski distance </b>
<br/> <br/>

<b> Models Used: <br/>

1) Logistic Regression
2) XgBoost
