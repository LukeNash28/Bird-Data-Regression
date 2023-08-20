# Factors Affecting Bird Behaviour

This project was created in order to illustrate how multinomial logistic regression modelling (MLR) can be used in the field of ecology. In this instance, MLR was used to attempt to quantify the extent to which the species of bird, the time of day it was recorded and the site at which it was recorded affected its behaviour. However, the analysis did not generate any quantifiably useful results due to the poor accuracy of the constructed model in spite of imbalance adjustments.

### Background Information

There are two .csv files in the repository containing the data used in the analysis. It was collected at two sites in the Silverdale Area of Outstanding Natural Beauty in Lancashire, NW England. These were: 
- [Leighton Moss][LM], a flagship RSPB reserve containing a mixed mosaic of tidal and freshwater wetlands, as well as extensive reedbeds, and;
- [Eaves Wood][EW], a patch of ancient woodland owned by the National Trust and a popular local walking spot.

The data was collected as part of a University of Durham field trip and its aim was to investigate the factors which affect bird behaviour. The scope of the analysis was left up to the individual students in the cohort for a summative analytical report written in early 2023.

### Data Collection and Data Cleaning Protocol

At both sites, birds encountered were identified to species using 8x42 binoculars, then counted, and their behaviour was recorded as one of three discrete categories: resting, foraging/feeding or travelling/flying. The time at which each bird was conducting this behaviour was also recorded. 

Within Microsoft Excel, all observations were then collated and standardised through standardisation of English names and correction of spelling errors and other misprints. The data were then filtered so that any observations which did not list a behavioural category, time or species were removed, as well entries where any of the variables were ambiguous (for example, multiple behavioural categories listed in one entry) and of observations deemed likely to involve significant observer error (e.g. misidentification).

The model construction process is described extensively in the Jupyter Notebook file in this repository. The analysis is not as exhaustive as I would usually like, but the poor data quality inferred from the model rendered further analysis counter-productive. This includes likelihood ratios to examine the relative significance of each of the covariates, and Poisson regression to investigate the extent to which each behavioural category was differentially impacted by the covariates.

### Evaluation

There were numerous issues with the data collection protocol and how it was conducted which merit mention. These include but are not limited to:

- The fact that only 9 species were recorded at both sites exacerbates both the difficulty in using taxonomic grouping in any modelling system and also the observed differences in behavioural patterns.
- Evidence of intra-specific variation in behaviour in some bird species - certainly a possible covariate, supported by several pieces of research, such as:
    -  Influence of microhabitat - remarkable asynchrony in breeding timing of Great Tits *Parus major* related to oak budding within just 20m of their breeding site in woodland habitats in Britain, thus causing a mosaic of Great Tit pairs at different stages of their breeding cycle even at the same site on the same day (Hinks, et al., 2015; Tong & Sheldon, 2020).
    -  Great Tit exploration behaviour is also likely to be governed by individuality, both in average level of exploration and its plasticity (Dingemanse, et al., 2012);
    -  Effects of habituation and other anthropogenic practices on bird behaviour (Dong & Clayton, 2009). 
    -  The group-size effect - vigilance behaviour decreases with increased group size, which increases the amount of time spent engaging in other behaviours; however, a broad array of other variables are thought to confound the group-size effect and as such its power as a covariate is potentially limited (Elgar, 1989).
- Highly arbitrary categorisation of behaviour - certain behavioural responses do not fit the categories used; for instance, many singing birds were recorded as resting, a categorisation that is questionable given the apparent increase in metabolic cost of singing compared to resting in passerines (Oberweger & Goller, 2001). 
- The behaviour of some species also leaves differentiation between each behavioural category open to interpretation; in hirundines, for example, differentiation of foraging and travelling can be difficult, especially on brief views, given many hirundines’ high propensity for aerial feeding and a lot of prey being taken whilst on the wing (Cramp, et al., 1993). 
- Observations were conducted by many different observers and there were no set guidelines for classification of ambiguous observations. 
- No agreed protocol for repeat counting and flushed birds, which certainly skewed the obtained data by omission or mis-categorisation of pertinent observations.
- Variation in prior ornithology experience among the observers may have created a detection bias, due to no instruction being given to novice observers on bird calls. This was something used by some observers with more experience to pick up a significant proportion of birds during the data collection, especially travelling ones. Species seen briefly were also far less likely to be identified, and consequently recorded, by the novices compared to the experienced observers.

Consequently, the data quality is likely to have been severely impacted, which in turn limits the generalizability and the utility of this research.


[//]: #

   [LM]: [https://www.rspb.org.uk/reserves-and-events/reserves-a-z/leighton-moss/]
   [EW]: [https://www.nationaltrust.org.uk/visit/lake-district/arnside-and-silverdale/eaves-wood-circular-walk]
 
