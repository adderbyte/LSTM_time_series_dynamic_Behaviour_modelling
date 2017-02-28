# Semester Project
      
      Project Title: Modelling Dynamic Temporal Behaviour Using Recurrent Neural Networks: AIR POLLUTION AS A CASE STUDY.
      BY           : Lukman Olagoke Olabisi.
      LAB          : Artificial Intelligence Lab EPFL, Switzerland.
      Date         : 2017 Spring Session.

---------------------------------------
Background
---------------------------------------
This project counts as a Semester Project which is part of the requirement for a Master Degree in Communication Systems at Ecole Plytechnique Federale de Laussane. 

      
---------------------------------------------------------------------------------------------------------------------------
Introduction
---------------------------------------------------------------------------------------------------------------------------   
The project is about Modelling Dynamic behaviour using Recurrent Neural Network. In particular we will be using Long Short term memory in this project (as an example of RNN) implemented using TensorFlow. Using these tools we will model and forecast Air pollution/ Air quality index of various countries and cities.  

-----------------------------------------------------------------------------------------------------------------------------
Important Domain Knowledge for the project
-----------------------------------------------------------------------------------------------------------------------------
Important domain knowledge used in this project: 

	1) Fundamentals of Air Pollution.
	2) Simple epidermic spread Model.
	3) Recurrent Neural Network (Long Short Term Memory)
	


---------------------------------------------------------------------------------------------------------------------------
Aims And Objectives
---------------------------------------------------------------------------------------------------------------------------

	1) Collect data from various sources and do  data-preprocessing 
	2) Use LSTM/time series analysis  to predict air pollution 
	3) Provide good visualisation of the results 
	4) Model the relationship/correlation between air pollution and epidermic spread.
	5) Use air pollution forecast to track epidermic cases in urban areas
	6) Use the air pollution and epidermic tracking models to help in decision making for preventing disease spread
	7) Implement simple Mobile apps that incorporates air polluton modelling and epidermic spread tracking.

---------------------------------------------------------------------------------------------------------------------------
Using this Repo
---------------------------------------------------------------------------------------------------------------------------
The following order is perhaps recommended for assessing the files provided in this repo:

	1) Air Pollution Essentials
	2) Tensor Flow Tutorial
	3) LSTM/ RNN

	
----------------------------------------------------------------------------------------------------------------------------
Optimal Model Selection Workflow.
-----------------------------------------------------------------------------------------------------------------------------
Below we provide a graphical representation of the task flow. 

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
      


-----------------------------------------------------------------------------------------------------------------------------
Resources
-----------------------------------------------------------------------------------------------------------------------------

1) Abshiskey Tiwary and Jeremy Colls (2002), *Air Pollution : measurement, Modelling and Mitigation*, Routledge Taylor and Francis group , London and New York.

2) Paolo Zanetti (1990) , *Air Plollution Modelling: Theories, Computational Methods and Available Software*, Computation Mechanics Publications, Bookcraft Ltd, Avon, Uk. 
      
3) https://www.airnow.gov/index.cfm?action=aqibasics.aqi

4) https://aqicn.org/faq/2015-03-15/air-quality-nowcast-a-beginners-guide/
