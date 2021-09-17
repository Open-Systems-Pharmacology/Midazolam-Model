### 2.3.1 Absorption

The model parameter `Specific intestinal permeability` was optimized to best match clinical data (see  [Section 2.3.4](#234-automated-parameter-identification)). The default solubility was assumed to be the measured value in FaSSIF (fasted state simulated intestinal fluid, see [Section 2.2.1](#221-in-vitro-and-physicochemical-data))

The dissolution of tablets were implemented via an empirical Weibull dissolution tablet. However, dissolution does not seem to be relevant in terms of *rate-limiting* kinetics; see results of optimization in [Section 2.3.4](#234-automated-parameter-identification).

### 2.3.2 Distribution

Midazolam is moderately to highly protein bound (approx. 97 %) in plasma (see [Section 2.2.1](#221-in-vitro-and-physicochemical-data)). A value of 3.1% was used in this PBPK model for `Fraction unbound (plasma, reference value)`. It was assumed that the major binding partner is albumin.

An important parameter influencing the resulting volume of distribution is lipophilicity. The reported experimental logP values are in the range of 3 (see [Section 2.2.1](#221-in-vitro-and-physicochemical-data)) which served as a starting value. Finally, the model parameters `Lipophilicity` was optimized to match best clinical data (see also [Section 2.3.4](#234-automated-parameter-identification)).

After testing the available organ-plasma partition coefficient and cell permeability calculation methods built in PK-Sim, observed clinical data was best described by choosing the partition coefficient calculation by `Rodgers and Rowland` and cellular permeability calculation by `PK-Sim Standard`.

Initial model building showed that the late disposition (approx. 24 hours after administration) could not be well described. This effect was assumed to be (re-)distribution-related. Finally, binding to a hypothetical binding partner in the brain was assumed (motivated by the target of midazolam: GABA receptor). After implementation of *in vitro* binding affinity to GABRG2 (Gamma-Aminobutyric Acid Type A Receptor Subunit Gamma 2) (see [Section 2.2.1](#221-in-vitro-and-physicochemical-data)), the  `Reference concentration` of GABRG2 was optimized to match best clinical data (see also [Section 2.3.4](#234-automated-parameter-identification)). Note that the respective `koff` value was assumed to be 1 min<sup>-1</sup>.

### 2.3.3 Metabolism and Elimination

Two metabolic pathways were implement into the model via Michaelis-Menten kinetics 

* CYP3A4
* UGT1A4

The CYP3A4 expression profiles is based on high-sensitive real-time RT-PCR ([Nishimura 2013](#5-references)). UGT1A4 was assumed to be exclusively expressed in the liver. Absolute tissue-specific expressions were obtained by considering the respective absolute concentration in the liver. The PK-Sim database provides a default value for CYP3A4 (compare [Rodrigues 1999](#5-references) and assume 40 mg protein per gram liver). A reference concentration of 2.32 µmol/L in the liver for UGT1A4 was derived from a quantification reported by Achour *et al.* ([Achour 2014](#5-references)) with 58.0 pmol/mg in Human Liver Microsomes (assuming 40 mg protein per gram liver).

Additionally, a renal clearance (assumed to be mainly driven by glomerular filtration) was implemented.

The first model simulations showed that gut wall metabolism was underrepresented in the PBPK model. In order to increase gut wall metabolism, the “mucosa permeability on basolateral side” (jointly the model parameters in the mucosa: ``P (interstitial->intracellular)`` and ``P (intracellular->interstitial)``) was estimated. A decrease in this permeability may lead to higher gut wall concentrations and, in turn, to a higher gut wall elimination. This parameter was preferred over other parameters such as relative CYP3A4 expression or fraction unbound (fu) in the gut wall as it is technically not limited to a maximum value of 100%.

### 2.3.4 Automated Parameter Identification

This is the result of the final parameter identification for the base model:

| Model Parameter                                              | Optimized Value                                              | Unit      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | --------- |
| `Lipophilicity`                                              | 2.897                                                        | Log Units |
| `Specific intestinal permeability`                           | 1.555E-4                                                     | cm/min    |
| Basolateral mucosa permeability<br />(``P (interstitial->intracellular)``, ``P (intracellular->interstitial)``) | 1.924E-3                                                     | cm/min    |
| `Km` (CYP3A4)                                                | 4 FIXED (see [Section 2.2.1](#221-in-vitro-and-physicochemical-data)) | µmol/L    |
| `kcat` (CYP3A4)                                              | 8.761                                                        | 1/min     |
| `Km` (UGT1A4)                                                | 37.8 FIXED (see [Section 2.2.1](#221-in-vitro-and-physicochemical-data)) | µmol/L    |
| `kcat` (UGT1A4)                                              | 3.591                                                        | 1/min     |
| `GFR fraction`                                               | 0.6401                                                       |           |
| `Reference concentration` (GABRG2)                           | 1.088<sup>*</sup>                                        | µmol/L    |

<sup>*</sup> The value in the model was updated to 1.041 with the release of PK-Sim 10 to account for the updated calculation method of interstitial concentrations (please refer to the respective [release notes of version 10](https://github.com/Open-Systems-Pharmacology/Suite/releases/tag/v10.0)).



This is the result of the final parameter identification for the dissolution parameters of a midazolam tablet:

| Model Parameter                    | Optimized Value | Unit |
| ---------------------------------- | --------------- | ---- |
| `Dissolution time (50% dissolved)` | 0.0107          | min  |
| `Dissolution shape`                | 4.3803          |      |