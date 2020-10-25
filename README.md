# Detecting-Hate-Speech & Offensive-Language-on-Twitter

### INTRODUCTION OF THE PROJECT

A key challenge for automatic hate-speech detection on social media is the separation of hate speech from other instances of offensive language. What constitutes hate speech and when does it differ from offensive language? No formal definition exists but there is a consensus that it is speech that targets disadvantaged social groups in a manner that is potentially harmful to them (Jacobs and Potter 2000; Walker 1994). In the United States, hate speech is protected under the free speech provisions of the First Amendment, but it has been extensively debated in the legal sphere and with regards to speech codes on college campuses. In many countries, including the United Kingdom, Canada, and France, there are laws prohibiting hate speech, which tends to be defined as speech that targets minority groups in a way that could promote violence or social disorder. People convicted of using hate speech can often face large fines and even imprisonment. These laws extend to the internet and social media, leading many sites to create their own provisions against hate speech. Both Facebook and Twitter have responded to criticism for not doing enough to prevent hate speech on their sites by instituting policies to prohibit the use of their platforms for attacks on people Copyright c 2017, Association for the Advancement of Artificial Intelligence (www.aaai.org). All rights reserved. based on characteristics like race, ethnicity, gender, and sexual orientation, or threats of violence towards others. Drawing upon these definitions, we define hate speech as language that is used to expresses hatred towards a targeted group or is intended to be derogatory, to humiliate, or to insult the members of the group. In extreme cases this may also be language that threatens or incites violence, but limiting our definition only to such cases would exclude a large proportion of hate speech. Importantly, our definition does not include all instances of offensive language because people often use terms that are highly offensive to certain groups but in a qualitatively different manner. For example some African Americans often use the term n*gga2 in everyday language online (Warner and Hirschberg 2012), people use terms like h*e and b*tch when quoting rap lyrics, and teenagers use homophobic slurs like f*g as they play video games. Such language is prevalent on social media (Wang et al. 2014), making this boundary condition crucial for any usable hate speech detection system . Previous work on hate speech detection has identified this problem but many studies still tend to conflate hate speech and offensive language. In this paper we label tweets into three categories: hate speech, offensive language, or neither. We train a model to differentiate between these categories and then analyze the results in order to better understand how we can distinguish between them. Our results show that fine-grained labels can help in the task of hate speech detection and highlights some of the key challenges to accurate classification. We conclude that future work must better account for context and the heterogeneity in hate speech usage.

### PROJECT PROBLEMS

A key challenge for hate-speech detection on social media is the separation of hate speech from other instances of offensive language. Lexical detection methods tend to have low precision because they classify all messages containing particular terms as hate speech and previous work using supervised learning has failed to distinguish between the two categories. We used a crowd-sourced hate speech lexicon to collect tweets containing hate speech keywords. We use crowd-sourcing to label a sample of these tweets into two categories: those containing hate speech as negative and those with neither as neutral. We train a multi-class classifier to distinguish between these different categories. Close analysis of the predictions and the errors shows when we can reliably separate hate speech from other offensive language and when this differentiation is more difficult. We find that racist and homophobic tweets are more likely to be classified as hate speech but that sexist tweets are generally classified as offensive. Tweets without explicit hate keywords are also more difficult to classify. Various machine learning approaches have been made in order to tackle the problem of toxic language. Majority of the approaches deal with feature extraction from the text. Lexical features such as dictionaries and bag-of-words were used in some studies. It was observed that these features fail to understand the context of the sentences. N-gram based approaches were also used which shows comparatively better results. Although lexical features perform well in detecting offensive entities, without considering the syntactical structure of the whole sentence, they fail to distinguish sentences ‘offensiveness which contain same words but in different orders.
Linguistic features such as parts-of-speech has also been used in hate speech detection problem, as shown in ; these approaches consist in detecting the category of the word, for instance, personal pronoun (PRP) and Verb non-3rd person. There have been several studies on sentiment-based methods to detect abusive language published in the last few years. One example is the work which applies sentiment analysis to detect bullying in tweets and use Latent Dirichlet Allocation (LDA) topic models to identify relevant topics in these texts. 

### KEY CONTRIBUTIONS

The review on the related work done in this field shows that the models trained after extracting N-gram features from text give better results . Also, the TFIDF approach on the bag of-words features also show promising results. Based on the review of features and the prominent classifiers used for text classification in the past work, we decided to extract n-grams from the text and weight them according to their TFIDF values. We feed these features to a machine learning algorithm to perform classification. Given the set of tweets, the aim of this work is to classify them into two categories: Negative and Neutral.

