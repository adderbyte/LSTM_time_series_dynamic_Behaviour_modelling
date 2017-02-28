-------
## Long Short Term Memory
------

<p> In this folder we implement long short term memory for air quality prediction. We will generally folllow the flow graph that is presented below.</p>


## Proposed Model




![Alt text](http://g.gravizo.com/svg?
  digraph G {
   aize ="2,4";
   Data [shape=box];
   HMM [shape = ellipse,style=filled,color=".7 .3 1.0"]
   LSTM [shape = ellipse,style=filled,color=".7 .3 1.0"]
   Data->{HMM;LSTM}
   Output [shape=box]
   HMM_STATE [shape=box]
   Output ->HMM_STATE
   HMM_STATE -> Output
   LSTM -> Output
   HMM -> HMM_STATE;
   Linear [style=filled,color=".7 .3 1.0"];
   Linear [shape = ellipse];
   {Output;HMM_STATE} -> {Linear};
   Prediction [ shape = box]
   {Linear} -> {Prediction};
   Output [label="LSTM output"];
   LSTM [label="Tree-based or Conv LSTM"];
   HMM_STATE [label="HMM State Probabilities"];
  }
) 

---
# Reference
---
<p>Vrakovna,Finale(2016), <i>Increasing the Interpretability of Neural Networks Using Hidden Markov Chains</i> 2016 ICML Workshop on Human Interpretability in Machine Learning</p>

