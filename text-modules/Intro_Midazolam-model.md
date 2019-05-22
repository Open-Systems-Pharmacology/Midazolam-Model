### Midazolam model

Midazolam is a widely-used sedative, approved as premedication before surgical interventions. It is almost exclusively metabolized by CYP3A4, turning it into a sensitive probe and victim drug for the investigation of in vivo CYP3A4 activity. Midazolam shows substantial first pass metabolism, resulting in a bioavailability of under 50%. Less than 1% of a midazolam dose is excreted unchanged in urine.

The herein presented model represents an update of the midazolam model publisdhed by Hanke et al. [[1](#reference)]. The model has been  developed using in particular published pharmacokinetic clinical data by Hohmann et al. 2015 [[2](#reference)], Hyland et al. 2009 [[3](#reference)] and Thummel et al. 1996 [[4](#reference)]. It has then been evaluated by comparing observed data to simulations of a large number of clinical studies covering a dose range from 0.05 mg/kg to 20 mg after intravenous and oral administrations. Furthermore, it has been evaluated within a CYP3A4 DDI modeling network as a victim drug. 

Model features include:

- CYP3A4 metabolism
- (direct) UGT1A4 metabolism
- excretion into urine via glomerular filtration
- a decrease in the permeability between the intracellular and interstitial space  (parameters "P (intracellular->interstitial)" and "P (interstitial->intracellular)") in intestinal mucosa to optimize quantitatively the extent of gut wall metabolism
- and binding to a hypothetical binding partner in the brain to optimize a late redistribution phase in midazolam plasma concentrations.

For further references please refer to the midazolam model repository [[5](#reference)] and the database of observed data [[6](#reference)].



#### References

[1] [Hanke N, Frechen S, Moj D, Britz H, Eissing T, Wendl T, Lehr T. PBPK models for CYP3A4 and P-gp DDI prediction: a modeling network of rifampicin, itraconazole, clarithromycin, midazolam, alfentanil and digoxin. CPT: Pharmacometrics & Systems Pharmacology (2018)](https://ascpt.onlinelibrary.wiley.com/doi/abs/10.1002/psp4.12343)

[2] [Hohmann N, Kocheise F, Carls A, Burhenne J, Haefeli WE, Mikus G. Midazolam microdose to determine systemic and pre-systemic metabolic CYP3A activity in humans. Br J Clin Pharmacol (2015)](https://doi.org/10.1111/bcp.12502)

[3] [Hyland R, Osborne T, Payne A, Kempshall S, Logan YR, Ezzeddine K, Jones B. In vitro and in vivo glucuronidation of midazolam in humans. Br J Clin Pharmacol (2009)](https://doi.org/10.1111/j.1365-2125.2009.03386.x)

[4] [Thummel KE, O'Shea D, Paine MF, Shen DD, Kunze KL, Perkins JD, Wilkinson GR. Oral first-pass elimination of midazolam involves both gastrointestinal and hepatic CYP3A-mediated metabolism. Clin Pharmacol Ther (1996)](https://doi.org/10.1016/S0009-9236(96)90177-0)

[5] [https://github.com/Open-Systems-Pharmacology/Midazolam-Model](https://github.com/Open-Systems-Pharmacology/Midazolam-Model)

[6] [https://github.com/Open-Systems-Pharmacology/Database-for-observed-data](https://github.com/Open-Systems-Pharmacology/Database-for-observed-data)

