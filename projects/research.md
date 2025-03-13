---
layout: post
title: 'Research'
---

Please check out my [Google Scholar page](https://scholar.google.com/citations?user=tmKKPjkAAAAJ) for a complete list of these works, full author lists for all works, and links to PDFs.

Here, I'll provide a short overview of each work and what I learned while working on it.


## Phi-2 and Phi-3

Phi-2 and Phi-3 were an absolute blast to work on. I'm ecstatic about both what these models represent for the future of AI and about the reception of these models from the community.

To me, these models represent a shift for LLMs by putting a larger and larger emphasis on high-quality data and combining that with targeted synthetic data generation. 

In my opinion, using the term "synthetic generation" doesn't quite do the data justice. I believe the future of synthetic generation for models entails thinking about generation in a new way - sculpting text samples over many rounds of iteration. This is beyond simply getting the response from a model to a fixed, single-round prompt. Instead, we can push a model to generate high-quality data from scratch about nearly anything.

I enjoyed working on various pieces of these models, including post-training, data generation, and even some parts of pre-training.

Besides the technical details, it was invaluable for me to learn how to be a part of a large team training one model. This kind of project is very different than a group of 2-5 people writing a paper. In many ways, I've gone full circle - my engineering background often helped me significantly in these projects. 

To build models, we must blend engineering and research. Organizationally, this work is weird. Software engineering is radically different to more traditional engineering, AI research is radically different to more traditional research. Here, we need to successfully do both.



## AI Platform



After the "internal rotation", I transitioned to an internal applied research team known as AI Platform. On this team, I worked on many projects, ranging from direct product work to research.
<!-- 
#### Direct Nash Optimization: Teaching Language Models to Self-Improve with General Preferences
##### Co-Author
##### Preprint, 2024

Add description for this

#### Efficient RLHF: Reducing the Memory Usage of PPO
##### Preprint, 2023 

Add description foor this

-->

#### What Matters In The Structured Pruning of Generative Language Models?
##### Preprint, 2023

I've always loved network compression as it requires asking interesting questions (and finding interesting answers). In this paper, we developed a method for pruning models based on "neuron uniqueness". 

At the time, there were many methods for pruning models, but they mostly centered around considering all network neurons independently of each other, for example, how much does neuron A affect the final output. We wanted to instead ask the question: how _unique_ is neuron A compared to all the other neurons, and if it is highly unique, is it more important to keep it when pruning?

Beyond this question, we had an additionally interesting finding - simply pruning weights randomly performed almost as well as some other state-of-the-art pruning methods! This was further evidence that pruning methods were looking at the wrong thing.

Overall, I love this work, but in retrospect it could use a lot of love. Better experiments, more solid evidence, and following up on some obvious questions. Still, I'm proud of it overall, and it may be worth re-visiting this concept in the future.



## Microsoft Research



After graduating, I started at Microsoft as a SWE. Quickly, I realized I wanted to get back into research. However, this is much easier said than done without a PhD and I spent a long time trying to break into research without success.

#### Efficient Computation of Deep Nonlinear Infinite-Width Neural Networks that Learn Features 
##### Co-Author
##### ICLR 2022

Greg Yang very kindly allowed me to work with him on this incredibly cool project that was well beyond my depth. In a 6-month "internal internship", I rotated to MSR and worked with him.

This project was incredibly challenging and rewarding. I spent a long time understanding the Tensor Programs papers and finally contributed to this paper by running experiments and implementing the Pi-Projected architecture for a few models.

In this paper, we develop a method for exactly computing trainable, infinitely-wide neural networks. This is done by projecting the weights into a lower-rank (and finite) space. Interestingly, in this paradigm, training a network corresponds to appending more rows to these low-rank matrices, meaning the network gets larger over time.

We had even greater plans after this paper, from the [pilim repo](https://github.com/santacml/pilim) to a few side projects (can we directly do autograd on a pi-projected network instead of growing the rows of the matrices? Can we prune redundant, linearly dependent rows in the pi-projected network?).

However, in retrospect, I had bitten off more than I could chew at that time and did not accomplish many of these efforts. Overall, it was an incredible learning experience for me, and I'm forever grateful to Greg for providing me the room to try and grow.



## Master's degree research at UC



At UC, I was able to do a Bachelor's and a Master's of Science in Computer Engineering. For the thesis, did research on using neural networks for malware detection. I found that I absolutely love research - it is some of the most rewarding work I have ever done.

#### Detecting Malware Code as Video With Compressed, Time-Distributed Neural Networks
##### IEEE Access

This, by far, is the paper I'm most excited about from my time at UC. Being published in an open access journal with a good impact factor, I am optimistic the paper might get some good traction. It's [available here](https://ieeexplore.ieee.org/abstract/document/9145735).

While in retrospect it could use a more exciting name, the journal article summarizes the main highlights of my research. The concept of Malware as Video, the best networks that we were able to build, comparisons to seminal works, and Node-Distance Pruning. Our results out-preform all works that we were able to find while staying lean and extraordinarily practical.

In addition, out of my work, I believe Node-Distance Pruning may actually be one of the more important things I've done. I found it to be a highly effective algorithm and may shed new light on where to go with pruning neural networks. As a future project I would like to submit a PR to get Node-Dist integrated into a more popular neural network library.

Overall, the paper is incredibly gratifying. It feels beyond exciting that the culmination of my work out is there, in a format for others to read and hopefully build on. So many iterations and so much work went into this final paper and I am glad it was able to be published.

#### Neural Classification of Malware-As-Video with Considerations for In-Hardware Inferencing
##### M.S. Thesis

If you're interested in my work I highly recommend downloading my M.S. thesis, available [for free here](http://rave.ohiolink.edu/etdc/view?acc_num=ucin1554216974556897). It's the most complete and organized work I've written both in terms of my research and in terms of, well, everything I've ever done. The other papers I've written were cut out of the context of the broader picture and therefore, in my opinion, provide value but leave a lot of unanswered questions. Even if there is only one section that interests you, I'd recommend going straight to it and treating the other sections as possible answers to other questions that come up.

I thoroughly enjoyed the process of assembling the work for, and writing, a thesis! 

#### A Foray Into Extracting Malicious Features from Executable Code with Neural Network Salience
##### NAECON 2019

Chronologically, the work that this paper came from happened last in my time at UC, though it ended up being published sooner due to long review times on the other papers. It is [available here](https://ieeexplore.ieee.org/abstract/document/9057859).

I love this paper. It's highly interesting and offers a ton of future work possibilities. Essentially, with saliency, we can see what the networks found to be unique to malware or benign code. This is a fruitful result - what were the commands that were unique to malware or benign code? Can we use these code clusters for a different, faster classification method and cut out the networks altogether? How would saliency differ from Malware as Image methods as compared to Malware as Video?

This short paper, in my mind, raises many interesting questions. It was a great, short project to wrap up my research with at UC as it leaves the door open for future work. There is still so much left to uncover with neural networks and I'm excited to see what the future brings.

#### Detecting Malicious Assembly using Convolutional, Recurrent Neural Networks
##### ASTESJ

ASTESJ invited us to write a paper extending our work done in the NAECON 2017 paper, which was our first neural network attempt. I'd like to discuss the journal itself. If one searches ASTESJ they will find some accusations of misconduct/unethical publishing, which was worrisome for me especially as someone young in their career. After consideration, we decided to write a paper on the recurrent neural networks we attempted to use for malware detection, which is available [here for free](https://astesj.com/v04/i05/p06/). 

There are not many papers using recurrent neural networks in this way - our (my) intention was not to get an easy publish, but to contribute some information that would not go into other papers we submit and be otherwise assumed knowledge without justification. I've been apprehensive about the journal, however, all my interactions with the journal were professional, the other papers in the journal seem credible, and others vouch for the integrity of the journal. Therefore, my conclusion at the moment is that the journal is simply young and still growing.

In my eyes, the work should speak for itself, regardless of the journal it appears in. This paper was important for establishing that while recurrent neural networks can work for this solution, they are not at all necessary or optimal. I'm happy with how the paper came out!

#### Detecting Malicious Assembly with Deep Learning
##### NAECON 2018

Work began for my research by replicating the results of others with a simple approach, and the first paper we wrote based on that work was presented at NAECON in 2017. The paper is available [here](https://ieeexplore.ieee.org/document/8556657).

There are honestly a multitude of things I would change about that first paper. If I could rewrite it, I would tie in more sources, better present the results of the paper as the figures are lacking, more thoroughly test the networks in various ways, and re-word large portions of it for clarity. At the same time, everyone starts somewhere and I'm glad to have been able to write that conference paper at all. I learned much from this paper and believe that the results of that learning can be seen in the works above.

