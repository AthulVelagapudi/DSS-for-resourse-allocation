# Decision support system for resourse allocation in covid
Overview
1. Project motivation
2. Problem Description 
3. Solution Architecture
4. Implementation
5. Conclusion
6. GUI
8. References
## Project motivation
Covid 19 has had a successful year considering how the situation has turned out in India after the second wave with around 300K cases per day. It was nothing short of a disaster. However, it wasn’t surprising, considering the safety measures like lockdowns and curfews. People were heavilyaffected by the lockdowns.

Resource distribution became a priority after the second wave since there was a massive imbalance of supply. States like Kerala had abundant resources while Delhi and Maharashtra were falling short of bare essentials. The demand for resources like oxygen cylinders, vaccines increased tremendously. A decision support system will not
only ease the issue of resource distribution but will also reduce the overhead of the whole decision-making process.
Our model-based Decision support system predicts an appropriate risk level of a region by considering various parameters and gives a clear picture of the resource distribution.
## Problem Description 
The second wave of Covid 19 has resulted in a significant
shift in the demand for critical resources. There is a major
misallocation of resources and manpower. States with
worrisome rates of growth are understaffed or have a dearth
of resources, whereas other states have an abundance of
goods. To address this, a DSS can be developed, which will
aid in decision making by predicting the risk weight of a
state considering various parameters.
## Solution Architecture
1.Architecture
![Architecture](https://github.com/AthulVelagapudi/DSS-for-resourse-allocation/blob/main/images/Arch1.png)
2. DSS model

![DSS model](https://github.com/AthulVelagapudi/DSS-for-resourse-allocation/blob/main/images/Arch2.png)

the above figures represented implementation(dss model) and architecture of the Decision Support System.
## Implementation
Objectives:
1. Collecting appropriate data of all the states for a one
month period i.e April-May 2021.
2. Developing a Statistical model which helps in estimating
the risk class.
3. Creating a Graphical User interface for the user to interact
with the system.
4. Connecting a database for storing the predictions as well
as retrieving information on various states.

1) Data: We collected data from various sources like
covid19india.org, state/central government websites. In order
to collect the availability, demand, supply of different resources required and used by individual states.
To make sure that the data is well representative of our
problem we went with 17 decision making criteria.
The data was for 1 month starting from April 8th - May 8th.
Fig. 3. Preprocessing
2) Pre-Processing: There were few instances with null
values since we could not find any reliable sources for them.
To bring the values to a similar scale We used z-score
normalisation technique.
3) Model: Random Forest Classifier We went with RFC
since it goes really well with classification tasks It’s an ensemble model which takes the mode of the output of multiple
decision trees.
Random Forest Classifier reduces over-fitting.
4) Training: We trained the model on 75% of the data.
For validation, we used the remaining 25% of the data.
Performance measure - F1 score.
5) Evaluation: Considering the class imbalance i.e between
the three risk levels we obtained an accuracy of 92%.
It depicts how well the model has generalised over the data
and it indicates that there was not any kind of over/underfitting.
6) Application and Database: We used the Tkinter Graphical User Interface toolkit to create an interface through which
the decision-maker can interact with the model

## Conclusion
The model has been trained over a well defined,
representative dataset and can predict an appropriate
risk weight for different regions based on specific criteria
with high accuracy. Our model successfully shows the number
of resources required by a specific region.

## GUI
First the gui opens as follows:

![](https://github.com/AthulVelagapudi/DSS-for-resourse-allocation/blob/main/images/Gui1.png)

We can choose whether to calculate giving the detials or selecting the region to know stats

1.(i) To calculate

![](https://github.com/AthulVelagapudi/DSS-for-resourse-allocation/blob/main/images/calculate.png)

(ii) After calculating the result the recomendation

![](https://github.com/AthulVelagapudi/DSS-for-resourse-allocation/blob/main/images/Calculated_results.png)

2) (i)To view stats

![](https://github.com/AthulVelagapudi/DSS-for-resourse-allocation/blob/main/images/stats.png)

(ii)After selecting the region

![](https://github.com/AthulVelagapudi/DSS-for-resourse-allocation/blob/main/images/stats_result.png)

## References
1. C. in India: Latest Map and f. h. Case Count. (n.d.). Covid19india.
Retrieved May 10, 2021, “Coronavirus in india,”
2. M. . U. R. F. T. D. S.-r.-e. Yiu, T. (2021
3. f. h.-l. API Reference — scikit-learn 0.24.2 documentation. (n.d.). ScikitLearn. Retrieved.May 11, 2021
4. f. h. t. tkinter — Python interface to Tcl/Tk — Python 3.9.5 documentation. (n.d.). Docs.Python.Org. Retrieved May 15, 2021, “a,”
5. R. Couronne, P. Probst, and A.-L. Boulesteix, “Random forest versus ´
logistic regression: a large-scale benchmark experiment,” BMC bioinformatics, vol. 19, no. 1, pp. 1–14, 2018.
6. C. Strobl, A.-L. Boulesteix, A. Zeileis, and T. Hothorn, “Bias in random
forest variable importance measures: Illustrations, sources and a solution,”
BMC bioinformatics, vol. 8, no. 1, pp. 1–21, 2007.
