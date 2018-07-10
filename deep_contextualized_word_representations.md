Definition of technique

word representation that models both complex characteristics of word use and how these uses vary across linguistic contexts to model polysemy (the coexistence of many possible meanings for a word or phrase).

Use cases

* question answering
* textual entailment
* setiment analysis

Note: exposing the deep internals of the pre-trained network is crucial, allowing downstream models to mix different types of semi-supervised signals.  Which means this can be used on partial training.

Introduction 

At a high level we want:

* complex characteristics of word use - syntax and semantics
* how these uses vary across linguistic contexts - model polysemy

Key insight: Our representations differ from traditional word type embeddings in that each token is assigned a representation that is a function of the entire input sentence.

The how:  We use vectors derived from a bidirectional LSTM that is trained with a coupled language model objective on a large text corpus.

I think the high level is achieved in the following way:
* the bidirectional LSTM gives syntax and semantics 
* the language model gives model polysemy

Technique name:  Embeddings from Language Models (ELMo - boooo, you just wanted to call it elmo)

