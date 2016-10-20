# HPAI Models



###Estimation of the basic reproductive number (R~0~) for epidemic, highly pathogenic avian influenza subtype H5N1 spread [@WARD_2008]  

This paper uses data from 110 outbreaks of HPAI H5N1 in village poultry in Romania in May/June 2006. Using GIS-based nearest-neighbor counting, epidemic doubling time, and an SI model, the authors obtained estimates of R~0~ at the village level. 

- Using GIS the authors estimated an R~0~ of 2.14 and 1.95, using road distance and Euclidean distance to determine nearest neighbors, respectively. 

- Using SI modeling, assuming that all villages were susceptible and $\beta = (NC)/(SI)$ where C is the rate at which S villages become I, the authors arrived at an R~0~ of 2.68 and daily $\beta$ which significantly decreased throughout the epidemic. 

- Using epidemic doubling time, the authors arrived at an R~0~ of 2.21.

- Model de-populates all poultry from infected village.

- Model assumes flock-level period of infectiousness between 7-14 days, cites other studies with 11.3-12.3 and 8-13.8 days.

###Assessing the Potential Impact of Avian Influenza on Poultry in West Africa: A Spatial Equilibrium Analysis [@You_2007]

This paper uses a spatial equilibrium model to quantify the economic losses that would result from avian influenza outbreaks in West Africa, specifically modeling Nigeria in detail. In the most serious outbreak scenario, where avian influenza is spread widely along two migratory bird pathways in Nigeria and there is local transmission of the disease, the model predicts that the country's chicken production would fall by 21.1% at a cost of around $250 million USD in lost revenue. 

- The authors used FAO *Gridded Livestock of the World* spatial dataset to define poultry distribution. When they compared chicken density and population density, they found that < 4% of West African population lives in high density chicken areas -- most poultry in this region are raised in small backyard groups (< 50 chickens).

- The authors used wild bird flyways as proxy for high risk of avian influenza (using different buffer sizes), assuming that migratory birds transmit the virus to poultry. There was no transmission parameter, just risk buffers.  

- The authors' model only considers poultry-to-poultry and wildfowl-to-poultry transmission, no other human or livestock pathways. 

- This is an economic model which considers supply, demand, and income -- but not import/export of chickens. The demand parameter is "shocked" by the avian influenza outbreak, incorporating the psychological effect an outbreak would have on demand and the chicken economy.

###Modeling highly pathogenic avian influenza transmission in wild birds and poultry in West Bengal, India [@Pandit_2013]

The authors of this paper used a stochastic continuous time model to simulate introduction of H5N1 to poultry communities in West Bengal, India. Additionally, they performed a spatial cluster analysis of outbreaks, calculated R~0~ using three methods, and performed a logistic regression to identify significant predictors of H5N1 outbreaks.

- SIC-SIRS model for change in disease status of a poultry flock (Susceptible - Infectious - Culled) and wild birds (SIRS), unit of interest is the village, with an infectious period of 7 days.  

- Every village (n = 37,945) considered to have both poultry flock and wild birds; once a flock in a village is infected it is assumed entire village is infected and will be culled. 

- Transmission rate between wild birds and poultry communities ($1.00 * 10^{-8}$) was based on previous study of avian influenza dynamics in wild birds [@Vaidya_2012].

- Transmission rate between poultry communities was estimated from SI calculations of observations, similar to a previous paper [@WARD_2008], with a mean of 0.127 and exponentially distributed ($\mu = 0.122$).

- R~0~ calculations: 
    - 0.859 (0.326 SD) via  SI equations
    - 1.069 via observed doubling time 
    - 1.034 via simulation results

- No consideration of LPAI in model; only HPAI entering from wild bird groups.

###Conceptual Framework for Avian Influenza Risk Assessment in Africa: The Case of Ethiopia [@Goutard_2007]

This paper primarily deals with a Risk Assessment model for HPAI in Ethiopia (using atRISK software). The authors specifically target two lakes: (Ziway and Awassa) to be the centerpiece of their analysis, and use SEIR modeling to evaluate the consequences of possible outbreaks in poultry

- Wild bird pathways were used and the number of migratory birds potentially infected WMc or carrying the virus was calculated: WMc = WM x p, where WM is the number of birds and p follows a Pert distribution. 

- Probability of exposure (Pww) between wild resident birds (WR) and WMc as computed using Pww = WMc/WR.

- Wild resident birds exposed was calculated as WRexp = WR x Pww.

- WRexp was converted to density using lake satellite buffers.

- Relative risk of exposure for domestic poultry (Pwd) population was calculated as Pwd = WRexp / density of poultry.

- Authors acknowledge that a complete model requires both environmental transmission and infected poultry trade transmission. 

###Mapping the Likelihood of Introduction and Spread of Highly Pathogenic Avian Influenza Virus H5N1 in Africa, Ghana, Ethiopia, Kenya, and Nigeria using Multicriteria Decision Modeling [@greycite54493]  

This analysis creates disease maps using multicriteria decision modelling (MCDM) to identify regions where the relative likelihood of introduction and spread of HPAI H5N1 is high. 

- Not a method of quantifying risk, just comparing relative risk levels. 

- Includes table of risk factors for HPAI H5N1 specific to Africa:
  - Introduction of H5N1:
    - Wild Bird Flyways
    - Surface Water: wetlands and waterbodies
    - Cross-border Roads
    - Ports
    - Airports
  - Spread of H5N1:
    - Roads
    - Navigable Rivers
    - Poultry Density
    - Presence of poultry markets / cities
    - Natural Wetlands and Waterbodies
    - Irrigated Areas
    
- Used a panel of five members to define relative importance of each factor.

- Includes MCDM maps of Nigeria, Ethiopia and Kenya

###The potential spread of highly pathogenic avian influenza virus via dynamic contacts between poultry premises in Great Britain [@Dent_2011]

The authors of this paper construct a model to investigate whether a large outbreak of HPAI is possible in the poultry industry of Great Britain, and what type of parameters might lead to such an outbreak.

- Network model with nodes (n = 10,692) representing poultry premises housing more than 50 birds, and edges that represent connections between farms from owners, catching teams, or slaughterhouse teams traveling. 

- Movement parameters regarding personnel based on expert opinion. 

- Stochastic simulation model with Susceptible, Infected, Detected, and Culled compartments and a time step of one day.  

- RNG chooses premises to infect and a random date of infection (one of 886 days covered by cathing company data set) to seed the outbreak.

- If seed farm was not visited within 15 days of seeding, transmission limited to 'local spread'. 

- It is assumed that HPAI spread through air is limited to only 500m range, besides this 'local spread' there is no way for virus to be transmitted except through owners, catching teams, or slaughterhouse teams. 

- It is unclear how authors integrated some catching team species-specific catching probabilities into model. 

- Parameter for personnel transmission (for each of the three types of personnel) is changed in a stepwise fasion from 0 to 0.2 in 0.01 steps as well as 0.001, giving rise to 10,648 scenarios The authors state that 100 simulations were run for each scenario. 

- Protection zones and surveillance zones set up once a case is identified in model, cutting off personnel movement/transmission. 

- Logistic regression was performed to determine odds ratios for transmission rates that created secondary spread epidemics (outside of one premise) as well as parameters which led to larger (> 65 premises) versus smaller (< 25 premises) outbreaks. 

#Summary - In Progress
Most compartmental models operate on the village- or flock-level; I have been unable to find poultry - poultry compartmental modeling. The predominant form of analysis in this area of research seems to be spatial at this time. 







## References

<div id="refs"></div>
