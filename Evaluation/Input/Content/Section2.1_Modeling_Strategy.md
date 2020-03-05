The general concept of building a PBPK model has previously been described by Kuepfer et al. ([Kuepfer 2016](#5-References)) Regarding the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in adults was gathered from the literature and has been previously published ([PK-Sim Ontogeny Database Version 7.3](#5-References)). The information was incorporated into PK-Sim® and was used as default values for the simulations in adults.

The  applied activity and variability of plasma proteins and active processes that are integrated into PK-Sim® are described in the publicly available PK-Sim® Ontogeny Database Version 7.3 ([Schlender 2016](#5-References)) or otherwise referenced for the specific process.

First, a mean model was built using clinical data from single dose studies with intravenous and oral administration of midazolam by Hohmann et al. ([Hohmann 2015](#5-Reference)) (plasma concentration), Hyland et al. 2009 ([Hyland 2009](#5-References)) (fraction metabolized via UGT1A4), and Thummel et al. 1996 ([Thummel 1996](#5-References)) (fraction excreted into urine of unchanged drug). The mean PBPK model was developed using a typical European individual. The relative tissue-specific expressions of enzymes predominantly being involved in the metabolism of midazolam (CYP3A4 and UGT1A4) were considered. The CYP3A4 expression profiles is based on high-sensitive real-time RT-PCR ([Nishimura 2013](#5 References)). UGT1A4 was assumed to be exclusively expressed in the liver. Absolute tissue-specific expressions were obtained by considering the respective absolute concentration in the liver. The PK-Sim database provides a default value for CYP3A4 (compare [Rodrigues 1999](#5-References) and assume 40 mg protein per gram liver) as reported by Ohtsuki *et al.* ([Ohtsuki  2012](#5-References)).

A specific set of parameters (see below) was optimized using the Parameter Identification module provided in PK-Sim®. Structural model selection was mainly guided by visual inspection of the resulting description of data and biological plausibility.

Once the appropriate structural model was identified, additional parameters for tablet formulations were identified. 

The model was then verified by simulating furter clinical studies reporting pharmacokinetic concentration-time profiles of midazolam.

Details about input data (physicochemical, *in vitro* and clinical) can be found in [Section 2.2](#2.2-Data).

Details about the structural model and its parameters can be found in [Section 2.3](#2.3-Model-Parameters-and-Assumptions).



