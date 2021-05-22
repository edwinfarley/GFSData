# GFSdata: BRFSS Example

The empirical example in the A Bayesian Approach to Linking Data Without Unique Identifiers article (https://arxiv.org/abs/2012.00601) is based on a subset of 3,200 randomly selected participants from the 2001 Behavioral Risk Factor Surveillance System (BRFSS) data set. The participants were randomly selected only among those that had complete data on all of the variables used for the analysis. 

The original data set (samples) is partitioned into two files (samples1, samples2), in order to mimic the input data that is commonly available in file linkage applications. From the available variables in BRFSS, we identify a set of variables that exists in both files and are recorded accurately and variables that are exclusive to each of the files. The variables that appear in both files were used to create blocks. The blocking variables are the individual's sex, state of residence, geographic stratum, and the time of year the entry was recorded, with the year split into four 3-month periods. These chosen blocking variables represent generic measures that could plausibly be shared by two distinct data sets similar to the BRFSS data set. This blocking scheme results in 1725 blocks, 1073 of which contain a single one-to-one link. The remaining 652 blocks with more than 1 record in each file have an average of 3.26 records and a maximum of 24 records.

Source: Department of Health, Centers for Disease Control Human Services, and Prevention (CDC). Behavioral risk factor surveillance system survey data, 2001.

Full Contents:
| Columns | Description |
| ---------- | -------------- |
| GENHLTH | A measure of general health on a scale of 1 to 5. |
| PHYSHLTH | A measure of physical health on a scale of 1 to 30. |
| MENTHLTH | A measure of mental health on a scale of 1 to 30. |
| AGE | The respondent's age. |
| ALCDAY | The number of days a year the respondent drinks alcohol. |
| WEIGHT | The respondent's weight in lbs. |
| ASTHMA | Whether the respondent has asthma. |
| block | Blocking index. |

The permutations folder contains pre-computed permutations using Normal model (P.csv), Logistic model (P_log.csv and P_log_A.csv, which has uniform blocks removed), Joint model (P_joint.csv).
