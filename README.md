### GompertzFit: A Bayesian code for fitting Gompertz function
#############################################################################################

#### Preamble:

Please contact Xavier Bouteiller at xavier.bouteiller(at)u-bordeaux(dot)fr with bug reports or questions. 

For more details, you can read [this paper](https://www.cambridge.org/core/journals/seed-science-research/article/using-automated-sanding-to-homogeneously-break-seed-dormancy-in-black-locust-robinia-pseudoacacia-l-fabaceae/811101B9C7853FC8EC628BAB0A3E1EE4)

#### Readme:

Here I provide a R/JAGS fitting a Gompertz Function. Gompertz function is frequently used for fitting sigmoid curves as for germination rate.

This repository contains:
- Code of the model: **ModelGompertz**
- A sample data set: **SampleDataset.txt**

#### Description of the original experimental design:

A Gompertz curve or Gompertz function, named after Benjamin Gompertz, is a sigmoid function. It is a type of mathematical model for a time series, where growth is slowest at the start and end of a time period. The right-hand or future value asymptote of the function is approached much more gradually by the curve than the left-hand or lower valued asymptote, in contrast to the simple logistic function in which both asymptotes are approached by the curve symmetrically. It is a special case of the generalised logistic function. Reference : [Wikipedia](https://en.wikipedia.org/wiki/Gompertz_function).

Gompertz used are frequently used for modelling Biological process as germination curves, tumor growth or population growth in a limited space.

#### Model:

We used Gompertz function to modelize germination data. We constructed a germination curve of the fraction of germinated seeds _G(t)_ as a function of time _t_ (days after sowing). The model was fitted using a Bayesian procedure. 

<img src="https://latex.codecogs.com/gif.latex?G(t)=&space;D&space;e&space;^{&space;-e^{-b&space;(t&space;-&space;t_{m})}}" title="G(t)= D e ^{ -e^{-b (t - t_{m})}}" />

where parameter _D_ is the maximum germination rate, _b_ is the slope of the germination curve and <img src="https://latex.codecogs.com/gif.latex?t_{m}" title="t_{m}" /> is the time at the inflexion point.

### References:

Ritz, C., Pipper, C.B. and Streibig, J.C. (2013) Analysis of germination data from agricultural experiments. European Journal of Agronomy 45, 1–6.

Torres, M. and Frutos, G. (1989) Analysis of germination curves of aged fennel seeds by mathematical models. Environmental and Experimental Botany 29, 409–415.

#### Publication:

If you are using this code for fitting sigmoid funtions, please cite:

>Bouteiller XP, Barraquand F, Garnier-Géré P, Harmand N, Laizet Y, Raimbault A, Segura R, Lassois L, Monty A, Verdu C, Mariette S & Porté AJ (2018) No evidence for genetic differentiation in juvenile traits between Belgian and French populations of the invasive tree *Robinia pseudoacacia*. Plant Ecology and Evolution.

>Bouteiller XP, Porté AJ, Mariette S, Monty A (2017). Using automated sanding to homogeneously break seed dormancy in black locust (*Robinia pseudoacacia* L., Fabaceae). Seed Science Research. https://doi.org/10.1017/S096025851700015
