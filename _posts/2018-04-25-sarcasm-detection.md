---
layout:     post
title:      Sarcastic or not? (1/2)
date:       2018-04-25 11:21:29
summary:    understanding the problem.
categories: nlp
tags: [Machine Learning]
comment: true
---

> Benzema is the best player ever.

This is 100% pure sarcasm. Okay, there is no such thing as _100% pure sarcasm_ but what there is are sarcastic and non sarcastic sentences.
For example, as soon as you read the above statement about Benzema, you could decipher that this is a statement which is definitely not true and is somewhat ironic in a mocking way. Someone who watches football, and has game sense would know that this sentence was a satirical remark. Someone who does not watch football, might think of this statement as <span style="color: #1eb300;"> True. </span> Hence we can say, that sarcasm is relative and highly depends on the context.

Try to understand the complexity of this problem, we as humans, find it really difficult to understand sarcasm, like we can only understand sarcasm once we have an idea about what is the context it is being used in, and the body language, the tone of the voice. If we closely observe someone saying a sarcastic sentence, the pitch of the voice varies. When English speakers remark sarcasm with the word  _"Thanks!"_, they often use a nasal tone. The nasal tone shows a connection between sarcasm and extreme disgust. It is like the speaker does not only want to remove the word from the mouth but also from the nose! So so many factors contributing to sarcasm makes it really really difficult to understand sarcasm for us, as humans, let alone computers.

I took the NLP class this semester at college, which dealt with understanding how Natural Language Processing works and reading and understanding research papers which was something that I was not used to, as bookish knowledge and Youtube was the only source of knowledge so far. TBH it was the most interesting class in this semester compared to my otherwise boring core Electrical Engineering subjects _literally very boring, I slept through most of my lectures <del> or maybe it is because of the faculty </del>_ Coming back to the point, I decided to make a project using the Natural Language Processing techniques learnt in this class and the ML algorithms to <span class="bg-dark-gray white" style="padding:2 px;"> Detect Sarcasm in Tweets. </span>

I basically aimed to create something to solve the complex problem of detecting sarcasm in the tweets. Machines are typically programmed to read the text as it is. It understands anything based strictly on what it is. So, detecting sarcasm was a difficult task. The reason why I chose twitter was because of the abundance of data available for the training of the supervised model. The main motivation behind understanding sarcasm using machines was in order to have a better understanding of one's data. So that the product reviewing system which scrape the websites can collect better data to analyze their product impact, and so that one can actually understand what the other person is trying to say. As there is no vocabulary defined for sarcasm, it becomes a difficult task, that is something more complicated than a simple classification technique like a _Spam Detection ALgorithm_ which would simply learn the vocabulary associated with the spam emails and filter them from the rest.

Sarcasm has been a widely studied topic in linguistics. Due to the advancement in technology and availability of data across the world, Sarcasm Detection has witnessed some great interest from the sentiment analysis community and become an active research area. Basically, what we are trying to achieve can be summed down as follow:
> Aiming to implement a model that can detect Sarcasm in Tweets, using NLP and ML techniques.

### Methodology

The main idea behind understanding sarcasm was that the first part of a sarcastic sentence would have more Positive sentiment as compared to the second part which would be inclined towards more Negative Sentiment. Or we can say that, if (+)ve Sentiment  and (-)ve Sentiment words appear in close proximity, the sentence might be sarcastic.

Taking an example: <span style="padding:2 px; color: #595959"> Benzema is the best. </span> We see that BENZEMA is a negative sentiment<small>(trust me)</small> and "is the best" positive. Okay, not the best of the examples; so a better example will be something like this <span style="padding:2 px; color: #595959;"> I am so happy that I failed again. </span>. If we analyze the statement: positive sentiment will be _"happy"_ and the word with negative sentiment will be _"failed"_. They are in close proximity and hence we might say that this is a sarcastic sentence. We choose this as one of the features <small> (to be discussed later) </small> and let the classifier decide. This sentiment based approach is the key part of the method. The complete methodology can be somewhat visualized as below:

_![method](https://i.imgur.com/wlByWoL.png)_

I will be explaining the implementation part using the above image in detail in the next part <small> will come really soon </small>. Thanks for reading this.

Have a good day. :)
