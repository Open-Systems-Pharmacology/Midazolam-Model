# Midazolam-Model
Whole-body PBPK model of midazolam.

<p align="center">
  <img src="Midazolam.png">
</p> 



This repository contains:

- a PK-Sim snapshot (*.json) file of the current PBPK model
- static content (e.g. text blocks, *.md files) as inputs for an evaluation plan
- an evaluation plan (evaluation-plan.json) to create an evaluation report using the snapshot and static text blocks to display the performance of the model

**The latest release of the snapshot of the model, the evaluation plan and the static content can be found [here](../../releases/latest).**

**The latest release of the PK-Sim project model file and the respective evaluation report can be found [here](https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library/releases/latest).**



This midazolam model is intended to be used as victim drug in CYP3A4-mediated drug-drug interactions (DDI).

This whole-body PBPK model of midazolam has been  developed using in particular published pharmacokinetic clinical data by Hohmann et al. 2015 [[1](#references)], Hyland et al. 2009 [[2](#references)] and Thummel et al. 1996 [[3](#references)]. 
The model has then been evaluated simulating a large number of clinical studies and comparing with respective observed data. 

The presented model represents an update of the midazolam model presented by Hanke et al. [[4](#references)].
Additional features in this update are:

- direct UGT1A4 metabolism,
- a decrease in the permeability between the intracellular and interstitial space  (parameters "P (intracellular->interstitial)" and "P (interstitial->intracellular)") in intestinal mucosa to optimize quantitatively the extent of gut wall metabolism,
- and binding to a hypothetical binding partner in the brain to optimize a late redistribution phase in midazolam plasma concentrations.


## Code of conduct

Everyone interacting in the Open Systems Pharmacology community (codebases, issue trackers, chat rooms, mailing lists etc...) is expected to follow the Open Systems Pharmacology [code of conduct](https://github.com/Open-Systems-Pharmacology/Suite/blob/master/CODE_OF_CONDUCT.md#contributor-covenant-code-of-conduct).

## Contribution

We encourage contribution to the Open Systems Pharmacology community. Before getting started please read the [contribution guidelines](https://github.com/Open-Systems-Pharmacology/Suite/blob/master/CONTRIBUTING.md#ways-to-contribute). If you are contributing code, please be familiar with the [coding standard](https://github.com/Open-Systems-Pharmacology/Suite/blob/master/CODING_STANDARDS.md#visual-studio-settings).

## License

The model code is distributed under the [GPLv2 License](https://github.com/Open-Systems-Pharmacology/Suite/blob/develop/LICENSE).

## References

[1] [Hohmann N, Kocheise F, Carls A, Burhenne J, Haefeli WE, Mikus G. Midazolam microdose to determine systemic and pre-systemic metabolic CYP3A activity in humans. Br J Clin Pharmacol (2015)](https://doi.org/10.1111/bcp.12502)

[2] [Hyland R, Osborne T, Payne A, Kempshall S, Logan YR, Ezzeddine K, Jones B. In vitro and in vivo glucuronidation of midazolam in humans. Br J Clin Pharmacol (2009)](https://doi.org/10.1111/j.1365-2125.2009.03386.x)

[3] [Thummel KE, O'Shea D, Paine MF, Shen DD, Kunze KL, Perkins JD, Wilkinson GR. Oral first-pass elimination of midazolam involves both gastrointestinal and hepatic CYP3A-mediated metabolism. Clin Pharmacol Ther (1996)](https://doi.org/10.1016/S0009-9236(96)90177-0)

[4] [Hanke N, Frechen S, Moj D, Britz H, Eissing T, Wendl T, Lehr T. PBPK models for CYP3A4 and P-gp DDI prediction: a modeling network of rifampicin, itraconazole, clarithromycin, midazolam, alfentanil and digoxin. CPT: Pharmacometrics & Systems Pharmacology (2018)](https://ascpt.onlinelibrary.wiley.com/doi/abs/10.1002/psp4.12343)

