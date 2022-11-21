# CS226-Project-Fall22
# CM 226: Project proposal (Fall 2022)

Git Source: url src=https://isimr.notion.site/Project-Planning-cd7c28396f214de68bcbf920e175caa9
##    \item Title
    \item Team members
    \item Define the problem.
    \item What prior approaches have been proposed (related work)?     
    \item What is your approach  ?    
    \item How will you evaluate your approach and compare to prior work ?  
    \item Is code available for competing methods ?     
    \item What dataset(s) will you use  ? Are the datasets formatted and easy to use or do you need to process data ?  
\end{itemize}

## Project Prompt:
Predict disease risk from genome
sequence data
Given genome sequence (or genotype data)
and disease status, learn a predictor that is
accurate on new individual.
See Dataset 6 in google doc

Predict disease risk from genome
sequence data
Given genome sequence (or genotype data)
and disease status, learn a predictor that is
accurate on new individual.
Variations: What if the individual is from a
different population than the training data ?
What if individual data is not available but
summary data is available ?


\section{Disease Prediction: A Genomic Persepective}
\section{Team Members}
    \begin{list}
        
        \item {Masand, Simran; UID: 706085004}
        \item {Song, Serena}
        \item Thai, Vincent \\
    \end{list}
\section{Motivation}
\section{Literature Review}
\section{Methodology}
\section{Benchmarks}
\section{Data and Code}


\end{document}

## Project Pipeline (Tentative):
Sorry this is word vomit at the moment. Will clean it up tonight. ;-;

Ability to digest lipids plays a very big role in determining obesity risk. Our goal is to predict obesity risk, specifically risk related to lipid processing capability, based on genotype. 

First an ANOVA test will be used for the variable ratio of change in bw for HFD vs CD. The change in bw for CD will just be the average. The change in bw for HFD will be individual. The goal of this test is to show that there is a difference in the means for ratio of change across different strains.

Then we will use the regression models to help predict the final weight. Maybe 2? 1 for CD, one for HFD?
Sample splitting options
Def split between CD and HFD
Then, either random splitting or stratified. Leaning towards stratified.
For stratified, we divide by strain (ex. X strains for validation, Y strains for testing?)

Model details
Model type 1: 
Input: genotype 
Output: change in bw
We will have 2 models, one for CD mice and one for HFD mice. We then can rank the ratios for change in bw. (The higher the ratio, the more at risk the strain is). Theoretically, the output across the same strains and diet would be the same predicted change since they have the same genotype. Good for seeing which strains are more susceptible.

Model type 2:
Input: genotype + Initial weight of bias term. 
Output: final weight 


% %%%%
% This writeup must describe the problem, related work, and the proposed research (e.g. we plan to apply method X on data Z, we plan to modify method W). For the proposed research, you should think about data  you will use to evaluate your proposed method to prior methods (if simulated data, say how you plan to simulate. for real datasets, do you have access to the data? if you are comparing to a previous method, is the software/results available for you to compare ? ) and the metrics you will use in the comparison.
