This SleepRestrictionReinforcementLearning_README.txt file was generated on
2020-12-01 by ANDREAS GERHARDSSON

GENERAL INFORMATION
===============================================================================

1. Title of Dataset
Sleep Restriction and Reinforcement Learning 2020 - Data Analysis

2. Author Information
	A. Principal Investigator Contact Information
		Name: Johanna Schwarz
		Institution: Stockholm University
		Address: Department of Psychology, 106 91 Stockholm, Sweden
		Email: johanna.schwarz@su.se

	B. Associate or Co-investigator Contact Information
		Name: Andreas Gerhardsson
		Institution: Stockholm University
		Address: Department of Psychology, 106 91 Stockholm, Sweden
		Email: andreas.gerhardsson@su.se

	C. Alternate Contact Information
		Name: John Axelsson
		Institution: Stockholm University
		Address: Department of Psychology, 106 91 Stockholm, Sweden
		Email: john.axelsson@su.se

3. Date of data collection (single date, range, approximate date):
2016-07 - 2016-10

4. Geographic location of data collection:
Stockholm, Sweden

5. Information about funding sources that supported the collection of the data:
-

SHARING/ACCESS INFORMATION
===============================================================================

1. Licenses/restrictions placed on the data:
CC by 4.0

2. Links to publications that cite or use the data:
https://doi.org/10.1111/jsr.13236

3. Links to other publicly accessible locations of the data:
10.17045/sthlmuni.11955939

4. Links/relationships to ancillary data sets:
-
5. Was data derived from another source?

6. Recommended citation for this dataset:
Gerhardsson A, Porada K D, Lundström N J, Axelsson J & Schwarz J (2020) Data
from: Does insufficient sleep affect how you learn from reward or punishment? –
Reinforcement learning after two nights of sleep restriction.
10.17045/sthlmuni.11955939

DATA & FILE OVERVIEW

1. File List:
Sleep Restriction and Reinforcement Learning - Data Analysis
    | - data/
        | - pst_full_data.txt
    | - scripts/
        | - pst_cm_1_fit.R
        | - pst_cm_2_preanalysis.R
        | - pst_cm_3_analysis.R
        | - pst_kss.R
        | - pst_lp_rt.R
        | - pst_lp_winstay_loseshift.R
        | - pst_plot_fnc.R
        | - pst_supplementary.R
        | - pst_test_phase_rt.R
        | - pst_test_phase.R
        | - RL_regressors_1a.stan
        | - RL_regressors.stan

2. Relationship between files, if important:

Models, plots  and tables are produced by the scripts

3. Additional related data collected that was not included in the current data package:

Mean aggregation of two nights of actigraph data is provided in this data set

4. Are there multiple versions of the dataset? yes/no
No


METHODOLOGICAL INFORMATION
===============================================================================
1. Description of methods used for collection/generation of data:


2. Methods for processing the data:

win-stay and lose-shift was calculated for each participant by sleep condition
and symbol pair.

win-stay = 1 if stay = 1 and feedback = positive, else win-stay = 0.
lose-shift = 1 if stay = 0 and feedback = negative, else lose-shift = 0.

3. Instrument- or software-specific information needed to interpret the data:
Software and packages required to run analyses, install may also include other
package dependencies
R (https://www.r-project.org/)
    Packages:
    bayesplot - Gabry J, Mahr T (2019). “bayesplot: Plotting for Bayesian
Models.” Rpackage version 1.7.0 package version 1.7.0
    bayestestR - Makowski, D., Ben-Shachar, M., & Lüdecke, D. (2019). bayestestR:
  Describing Effects and their Uncertainty, Existence and Significance
  within the Bayesian Framework. Journal of Open Source Software,
  4(40), 1541. doi:10.21105/joss.01541
    brms - Paul-Christian Bürkner (2017). brms: An R Package for Bayesian Multilevel Models
  Using Stan. Journal of Statistical Software, 80(1), 1-28.
  doi:10.18637/jss.v080.i01
    ggplot2 - H. Wickham. ggplot2: Elegant Graphics for Data Analysis. Springer-Verlag New York,
  2016.
    ggpubr - Alboukadel Kassambara (2019). ggpubr: 'ggplot2' Based Publication Ready Plots. R
  package version 0.2.4. https://CRAN.R-project.org/package=ggpubr
    gridExtra - Baptiste Auguie (2017). gridExtra: Miscellaneous Functions for
"Grid" Graphics. R Graphics. R
  package version 2.3. https://CRAN.R-project.org/package=gridExtra
    plyr - Hadley Wickham (2011). The Split-Apply-Combine Strategy for Data Analysis. Journal
  of Statistical Software, 40(1), 1-29. URL http://www.jstatsoft.org/v40/i01/.
    rstanarm - Goodrich B, Gabry J, Ali I & Brilleman S. (2018). rstanarm: Bayesian applied
  regression modeling via Stan. R package version 2.17.4. http://mc-stan.org/
    see - Daniel Lüdecke, Dominique Makowski, Philip Waggoner and Mattan S. Ben-Shachar
  (2019). see: Visualisation Toolbox for 'easystats' and Extra Geoms, Themes and
  Color Palettes for 'ggplot2'. R package version 0.3.0.
  https://CRAN.R-project.org/package=see
    shinystan - Jonah Gabry (2018). shinystan: Interactive Visual and Numerical Diagnostics and
  Posterior Analysis for Bayesian Models. R package version 2.5.0.
  https://CRAN.R-project.org/package=shinystan
    wesanderson - Karthik Ram and Hadley Wickham (2018). wesanderson: A Wes Anderson Palette
  Generator. R package version 0.3.6.
https://CRAN.R-project.org/package=wesanderson

Software used to perform Probalisitic Selection Task
    Inquisit 4 (www.millisecond.com)

4. Standards and calibration information, if appropriate:
-

5. Environmental/experimental conditions:
Two nights of sleep restriction vs normal night sleep

6. Describe any quality-assurance procedures performed on the data:
see published article

7. People involved with sample collection, processing, analysis and/or submission:
see published article

DATA-SPECIFIC INFORMATION FOR: pst_full_data.txt
1. Number of variables:
42

2. Number of cases/rows:
13140

3. Variable List:
Variable // Description

Code // subject + sleep condition + order
subject // Subject ID
sleep // sleep condition character
sr // sleep restriction (1 = yes, =, no)
BaselineFirst // order of sleep condition (1 = normal sleep first, 0 = Sleep restriction first)
female // gender (1 = female, 0 = male)
age // Age in years
night // not relevant
days_between_tests // days between tests
testtime // time of test HH:MM:SS default origin
blockcode // block code of PST (learning phase or test phase)
blocknum // block number of PST (first block = 4)
trialcode // trial code of PST (symbol + order + phase)
trialnum // trial number, originally including all events (responses etc.)
stimulusitem1 // experiment path to symbol 1, not relevant for analysis, see Figur 1 in manuscript.
stimulusitem2 // experiment path to symbol 2, not relevant for analysis, see Figur 1 in manuscript.
values.winletter // which symbol to win
response_key // response key number on keyboard
values.selectedletter // symbol chosen
correct // correct during learning phase = positive feedback, during test phase = best option
response_time_ms // response time in milliseconds
expressions.percA_ab // cumulative proportion correct for symbol pair AB
expressions.percC_CD // cumulative proportion correct for symbol pair CD
expressions.percE_EF // cumulative proportion correct for symbol pair EF
Bed time // Bedtime according to actigraph
Get up time // get up time according to actigraph
Time in bed // Time in bed according to actigraph
Sleep start // Sleep start according to actigraph
Sleep end // Sleep end according to actigraph
Assumed sleep // Assumed sleep according to actigraph
Actual sleep time // Actual sleep according to actigraph (H:M:S)
Actual sleep (%) // Actual sleep percent according to actigraph
Actual wake time // Actual wake according to actigraph (H:M:S)
Actual wake (%) // Actual wake percent according to actigraph
Sleep efficiency // Sleep efficiency percent according to actigraph
Sleep latency // Sleep latency according to actigraph (H:M:S)
get_up_easy // sleep diary easy to get up (5 = very easy, 1 = very difficult)
well_rested // well rested after sleep (5 = fully, 1 = not at all)
KSS // Karolinska sleepiness scale
SUSS // Subjective stress scale
kss_rt_ms // Karolinska sleepiness scale, response time in milliseconds
stress_rt_ms // Subjective stress scale, response time in milliseconds

4. Missing data codes:
NA

5. Specialized formats or other abbreviations used:
-


// necessary
Code // subject + sleep condition + order
subject // Subject ID
sleep // sleep condition character
sr // sleep restriction (1 = yes, =, no)
BaselineFirst // order of sleep condition (1 = normal sleep first, 0 = Sleep restriction first)
female // gender (1 = female, 0 = male)
age // Age in years
blockcode // block code of PST (learning phase or test phase)
correct // correct during learning phase = positive feedback, during test phase = best option
response_time_ms // response time in milliseconds
Time in bed // Time in bed according to actigraph
Assumed sleep // Assumed sleep according to actigraph
Actual sleep time // Actual sleep according to actigraph (H:M:S)
Actual sleep (%) // Actual sleep percent according to actigraph
Actual wake time // Actual wake according to actigraph (H:M:S)
Actual wake (%) // Actual wake percent according to actigraph
Sleep efficiency // Sleep efficiency percent according to actigraph
Sleep latency // Sleep latency according to actigraph (H:M:S)
get_up_easy // sleep diary easy to get up (5 = very easy, 1 = very difficult)
well_rested // well rested after sleep (5 = fully, 1 = not at all)
KSS // Karolinska sleepiness scale
SUSS // Subjective stress scale
kss_rt_ms // Karolinska sleepiness scale, response time in milliseconds
stress_rt_ms // Subjective stress scale, response time in milliseconds