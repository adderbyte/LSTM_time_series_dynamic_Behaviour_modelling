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
	2) Statistical Analysis of data.
	3) Time series Forecast
	4) Recurrent Neural Network (Long Short Term Memory)
	


---------------------------------------------------------------------------------------------------------------------------
Aims And Objectives
---------------------------------------------------------------------------------------------------------------------------

	1) Collect data from various sources and do  data-preprocessing 
	2) Use LSTM/time series analysis  to predict air pollution 
	3) Provide good visualisation of the results 
	4) Model the relationship/correlation between air pollutants
	5) Deal with Missing data
	
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
digraphG{
aize="2,4";
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
![alt text](http://http://g.gravizo.com/svg?%20%20digraph%20G%20{%20%20%20aize%20=%222,4%22;%20%20%20node%20[shape=box,style=filled,color=%22.7%20.3%201.0%22];%20%20%20Data%20[shape=box];%20%20%20{Emission;Meteorology;AirQuality}-%3E%20Data%20%20%20AirQuality%20-%3E%20statEval;%20%20%20node%20[style=filled,weight=4,color=%22gray%22];%20%20%20Data%20-%3E%20cleaning%20;%20%20%20%20node%20[shape=box,style=filled,color=%22.7%20.3%201.0%22];%20%20%20cleaning%20-%3E%20ModelRuns;%20%20%20%20ModelRuns%20-%3E%20SimulatedConc;%20%20%20node%20[shape=ellipse]%20%20%20SimulatedConc%20-%3E%20statEval;%20%20%20node%20[shape=box,color=%22gray%22];%20%20%20statEval%20-%3E%20UsableModel%20;[style=bold,label=%22Yes%22,color=%22green%22];%20%20%20edge%20[color=red];%20%20%20statEval%20-%3E%20ModifyModel;[style=bold,label=%22No%22];%20%20%20%20ModifyModel%20-%3E%20cleaning;%20%20%20Data%20[label=%22Data%20Collection%22];%20%20%20cleaning%20[label=%22Definition%20of%20Model%20Parameters%22];%20%20%20ModelRuns%20[label=%22Model%20Runs%22];%20%20%20SimulatedConc%20[label=%22Simulated%20Concentrations%22];%20%20%20statEval%20[label=%22Statistical%20Evaluation%20ok?%22];%20%20%20UsableModel%20[label=%22Model%20can%20be%20used%20for%20decision%20Making%22];%20%20%20ModifyModel%20[label=%22Modify%20model%20inputs(Calibration)%22];%20%20%20AirQuality%20[label=%22Air%20Quality%22];%20%20})   
<p align="center">
  <img src="http://g.gravizo.com/svg?digraph%20G%20{aize=%222,4%22;node%20[shape=box,style=filled,color=%22.7%20.3%201.0%22];%20%20%20Data%20[shape=box];%20%20%20{Emission;Meteorology;AirQuality}-%3E%20Data%20%20%20AirQuality%20-%3E%20statEval;%20%20%20node%20[style=filled,weight=4,color=%22gray%22];%20%20%20Data%20-%3E%20cleaning%20;%20%20%20%20node%20[shape=box,style=filled,color=%22.7%20.3%201.0%22];%20%20%20cleaning%20-%3E%20ModelRuns;%20%20%20%20ModelRuns%20-%3E%20SimulatedConc;%20%20%20node%20[shape=ellipse]%20%20%20SimulatedConc%20-%3E%20statEval;%20%20%20node%20[shape=box,color=%22gray%22];%20%20%20statEval%20-%3E%20UsableModel%20;[style=bold,label=%22Yes%22,color=%22green%22];%20%20%20edge%20[color=red];%20%20%20statEval%20-%3E%20ModifyModel;[style=bold,label=%22No%22];%20%20%20%20ModifyModel%20-%3E%20cleaning;%20%20%20Data%20[label=%22Data%20Collection%22];%20%20%20cleaning%20[label=%22Definition%20of%20Model%20Parameters%22];%20%20%20ModelRuns%20[label=%22Model%20Runs%22];%20%20%20SimulatedConc%20[label=%22Simulated%20Concentrations%22];%20%20%20statEval%20[label=%22Statistical%20Evaluation%20ok?%22];%20%20%20UsableModel%20[label=%22Model%20can%20be%20used%20for%20decision%20Making%22];%20%20%20ModifyModel%20[label=%22Modify%20model%20inputs(Calibration)%22];%20%20%20AirQuality%20[label=%22Air%20Quality%22];%20%20})" width="350"/>
  
</p>

-----------------------------------------------------------------------------------------------------------------------------
Resources
-----------------------------------------------------------------------------------------------------------------------------

1) Abshiskey Tiwary and Jeremy Colls (2002), *Air Pollution : measurement, Modelling and Mitigation*, Routledge Taylor and Francis group , London and New York.

2) Paolo Zanetti (1990) , *Air Plollution Modelling: Theories, Computational Methods and Available Software*, Computation Mechanics Publications, Bookcraft Ltd, Avon, Uk. 
      
3) https://www.airnow.gov/index.cfm?action=aqibasics.aqi

4) https://aqicn.org/faq/2015-03-15/air-quality-nowcast-a-beginners-guide/
