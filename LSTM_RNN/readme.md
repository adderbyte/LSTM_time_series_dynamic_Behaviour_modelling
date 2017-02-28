-------
## Long Short Term Memory
------

<p> In this folder we implement long short term memory for air quality prediction</p>

------
## Proposed Model
_____





![Alt text](http://g.gravizo.com/svg?
  digraph G {
   aize ="2,4";
   node [shape=box,style=filled,color=".7 .3 1.0"];
   Data [shape=box];
   Data->{HMM;LSTM}
   node [style=filled,weight=4,color="gray"];
   node [shape=box,style=filled,color=".7 .3 1.0"];
   LSTM -> Output; 
   HMM -> HMM_STATE
   
   {Output;HMM_STATE} -> {Linear}
   {Linear} -> {Prediction}
   Output [label="LSTM output"];
   LSTM [label="VAriants of LSTM: (Tree LSTM or Conv LSTM)"];
   HMM_STATE [label="HMM state Probabilities"];
  }
) 
