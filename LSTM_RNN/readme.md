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
   {Emission;Meteorology;AirQuality}-> Data
   AirQuality -> statEval;
   node [style=filled,weight=4,color="gray"];
   Data -> cleaning ; 
   node [shape=box,style=filled,color=".7 .3 1.0"];
   cleaning -> ModelRuns; 
   ModelRuns -> SimulatedConc;
   node [shape=ellipse]
   SimulatedConc -> statEval;
   node [shape=box,color="gray"];
   statEval -> UsableModel ;[style=bold,label="Yes",color="green"];
   edge [color=red];
   statEval -> ModifyModel;[style=bold,label="No"]; 
   ModifyModel -> cleaning;
   Data [label="Data Collection"];
   cleaning [label="Definition of Model Parameters"];
   ModelRuns [label="Model Runs"];
   SimulatedConc [label="Simulated Concentrations"];
   statEval [label="Statistical Evaluation ok?"];
   UsableModel [label="Model can be used for decision Making"];
   ModifyModel [label="Modify model inputs(Calibration)"];
   AirQuality [label="Air Quality"];
  }
) 
