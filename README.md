# F1 Race Results Prediction Algorithm

Repository with R code for F1 Race Results Prediction Algorithm. 

Project used for double-degree-link program between:
- MSc Statistics Dissertation for University of Essex.
- BSc Applied Mathematics for Instituto Tecnológico Autónomo de México (ITAM).

Supervisors:
<a href="https://www.essex.ac.uk/people/salhi90905/abdellah-salhi">Professor Abdellah Salhi</a> (University of Essex) and <a href="https://agarbuno.github.io/">Dr. Alfredo Garbuno Iñigo</a> (ITAM).

## Licence
<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/dannescudero/F1GridPrediction">F1GridPrediction</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/dannescudero">Daniela Escudero Ambrosi</a> is licensed under <a href="http://creativecommons.org/licenses/by-nc/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-NC 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1"></a></p>

## Data
The data for this project comes from the `R` package, <a href="https://github.com/cran/f1dataR">f1dataR</a> created by <a href="https://github.com/SCasanova">Casanova</a> and <a href="https://github.com/pbulsink">Bulsink</a>. This `R` package gathers the data from the <a href="http://ergast.com/mrd/">Ergast Developer API</a>, an experimental web service which provides a historical record of motor racing data, and the official Formula 1 data stream via the <a href="https://pypi.org/project/fastf1/">fastf1</a> `Python` library.

## Abstract

This repository introduces a novel non-parametric model for predicting Formula 1 race outcomes, utilizing an adapted Elo rating system to estimate driver strengths. The model addresses the challenges posed by F1's complex multi-class outcomes and the absence of historical car update data. It outperforms alternative methods, including machine learning and neural networks, highlighting its adaptability for other sports and its potential to support the growing trend of F1 betting and analysis driven by a expanding fan base.

## List or Components
- `F1 I.Rmd` R markdown code with all functions
- `DataSetY.csv` Data Set of year Y with column values:
    - <em> driver_id: <em> drivers from the Y season;
    - <em> constructor_id: <em> constructor associated to the driver;
    - <em> round: <em> different races in the respective season, usually there are 22;
    - <em> grid: <em> is a value from 1 to 20 that states the position on which the driver starts the race;
    - <em> position: <em> is the number indicates the result of the race, ranging from 1 to 20;
    - <em> status: <em> explains the condition on which the drivers finalized the race. The focus is around two main concerns: for finished drivers or if an incident was presented;
    - <em> pos_gained: <em> refers to the variable computed as position - grid. The value ranges from -19 to 19 and states the final number of places the driver gained/lost;
    - <em> round_points: <em> the points awarded according to the race result (different from the original FIA ones);
    - <em> accum_points: <em> is the accumulated value of awarded points up to the ith race;
    - <em> PI: <em> is the Power Index which describes th epercentage of available points;
    - <em> PI_adj: <em> is the Adjusted Power Index associated to the previous PI
