The general concept of building a PBPK model has previously been described by Kuepfer et al. ([Kuepfer 2016](#5-references)). Relevant information on anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in adults was gathered from the literature and has been previously published ([Willmann 2007](#5-references)). The information was incorporated into PK-Sim® and was used as default values for the simulations in adults.

The applied activity and variability of plasma proteins and active processes that are integrated into PK-Sim® are described in the publicly available PK-Sim® Ontogeny Database Version 7.3 ([PK-Sim Ontogeny Database Version 7.3](#5-references)) or otherwise referenced for the specific process.

First, a mean model was built using clinical data from single dose studies with intravenous and oral administration of midazolam by Hohmann et al. ([Hohmann 2015](#5-references)) (reporting plasma concentrations), Hyland et al. 2009 ([Hyland 2009](#5-references)) (reporting the dose fraction metabolized via UGT1A4), and Thummel et al. 1996 ([Thummel 1996](#5-references)) (reporting the dose fraction excreted into urine of unchanged drug). The mean PBPK model was developed using a typical European individual. The relative tissue-specific expressions of enzymes predominantly being involved in the metabolism of midazolam (CYP3A4 and UGT1A4) were considered ([Meyer 2012](#5-references)).

A specific set of parameters (see below) was optimized using the Parameter Identification module provided in PK-Sim®. Structural model selection was mainly guided by visual inspection of the resulting description of data and biological plausibility.

Once the appropriate structural model was identified, additional parameters for tablet formulations were identified. 

The model was then verified by simulating further clinical studies reporting pharmacokinetic concentration-time profiles of midazolam.

Details about input data (physicochemical, *in vitro* and clinical) can be found in [Section 2.2](#22-data).

Details about the structural model and its parameters can be found in [Section 2.3](#23-model-parameters-and-assumptions).



