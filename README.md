# Semester Project
      
      Project Title: Modelling Dynamic Behaviour with LSTM: AIR POLLUTION AS A CASE STUDY.
      BY           : Lukman Olagoke Olabisi.
      LAB          : Artificial Intelligence LAb EPFL, Switzerland.
      Date         : 2017 Spring Session.

---------------------------------------
Background
---------------------------------------
This project counts as a Semester Project which is part of the requirement for a Master Degree in Communication Systems at Ecole Plytechnique Federale de Laussane. 

      
---------------------------------------------------------------------------------------------------------------------------
Introduction
---------------------------------------------------------------------------------------------------------------------------   
The project is about Modelling Dynamic behaviour using Recurrent Neural Network. In particular we will be using Long Short term memory in this project (as an example of RNN). The implementation will be carried out using Tensor Flow. We will be modelling Air pollution as an example of a real life phenomenon that can be modelled as a time series -  using LSTM and tensorflow as our forecasting and modelling tool.

---------------------------------------------------------------------------------------------------------------------------
Aims And Objectives
---------------------------------------------------------------------------------------------------------------------------

	1) Collect data from various sources and do  data-preprocessing 
	2) Use LSTM/time series analysis  to predict air pollution 
	3) Provide good visualisation of the results 
	4) Model the relationship/correlation between air pollution and epidermic spread.
	5) Use air pollution forecast to track epidermic cases in urban areas
      6) Use the air pollution and epidermic tracking models to help people in decision making for preventing epidermic spread
      7) Implement simple Mobile apps that incorporates air polluton modelling and disease spread.
      
  -----------------------------------------------------------------------------------------------------------------------------
Summary of Task Flow
-----------------------------------------------------------------------------------------------------------------------------
Below we provide a graphical representation of the task flow. 

![Alt text](http://g.gravizo.com/svg?
  digraph G {
   aize ="2,4";
   node [shape=box,style=filled,color=".7 .3 1.0"];
   Data [shape=box];
   Data -> cleaning [weight=4];[color="gray"];
   cleaning -> ModelRuns; 
   ModelRuns -> SimulatedConc;
   node [shape=ellipse,aize="0.9",weight=3];
   SimulatedConc -> statEval;
   node [shape=box,style=filled,color="gray"];
   statEval -> UsableModel ;[style=bold,label="Yes",color="green"];
   edge [color=red];
   statEval -> ModifyModel;[style=bold,label="No"]; 
   ModifyModel -> cleaning;
   Data [label="Data Collection"];
   cleaning [label="Definition of Model Parameters"];
   ModelRuns [label="Model Runs"];
   SimulatedConc [label="Simulated Concentrations"];
   statEval [label="Statistical Evaluation O.K?"];
   UsableModel [label="Model can be used for decision Making"];
   ModifyModel [label="Modify model inputs(Calibration)"];
  }
)    
      
      
      
      
      
