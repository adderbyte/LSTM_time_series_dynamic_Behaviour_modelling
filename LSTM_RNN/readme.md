-------
## Long Short Term Memory
------

<p> In this folder we implement long short term memory for air quality prediction</p>


## Proposed Model




![Alt text](http://g.gravizo.com/svg?
  digraph G {
   aize ="2,4";
   Data [shape=box];
   node [style=filled,color="#7CFC00"];
   HMM [shape = ellipse]
   LSTM [shape = ellipse]
   Data->{HMM;LSTM}
   node [style=filled,weight=4,color="white"];
   LSTM -> Output; 
   HMM -> HMM_STATE;
   node [shape=box,style=filled,color="#7CFC00"];
   {Output;HMM_STATE} -> {Linear};
   node [shape=box,style=filled,color="white"];
   {Linear} -> {Prediction};
   Output [label="LSTM output"];
   LSTM [label="Tree-based or Conv LSTM"];
   HMM_STATE [label="HMM state Probabilities"];
  }
) 
