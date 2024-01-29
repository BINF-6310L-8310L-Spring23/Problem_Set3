# Problem_Set4
Instructions for problem set 4

The goal of this problem set is to practice parametric tests on real-world data 

NASA has a very interesting Open Science Data Repository https://osdr.nasa.gov/bio/repo/search?q=&data_source=cgene,alsda&data_type=study

For this problem set we will use *OSD-488: Characterizing SERCA Function in Murine Skeletal Muscles after 35-37 Days of Spaceflight from RR-1 and RR-9*
https://osdr.nasa.gov/bio/repo/data/studies/OSD-488

The description of the study is below

*It is well established that microgravity exposure causes significant muscle weakness and atrophy via muscle unloading. On Earth, muscle unloading leads to a disproportionate loss in muscle force and size with the loss in muscle force occurring at a faster rate. Although the exact mechanisms are unknown, a role for Ca2+ dysregulation has been suggested. The sarco(endo)plasmic reticulum Ca2+ ATPase (SERCA) pump actively brings cytosolic Ca2+ into the SR, eliciting muscle relaxation and maintaining low intracellular Ca2+ ([Ca2+]i). SERCA dysfunction contributes to elevations in [Ca2+]i, leading to cellular damage, and may contribute to the muscle weakness and atrophy observed with spaceflight. Here, we investigated SERCA function, SERCA regulatory protein content, and reactive oxygen/nitrogen species (RONS) protein adduction in murine skeletal muscle after 35-37 days of spaceflight. In male and female soleus muscles, spaceflight led to drastic impairments in Ca2+ uptake despite significant increases in SERCA1a protein content. We attribute this impairment to an increase in RONS production and elevated total protein tyrosine (T) nitration and cysteine (S) nitrosylation. Contrarily, in the tibialis anterior (TA), we observed an enhancement in Ca2+ uptake, which we attribute to a shift towards a faster muscle fiber type (i.e., increased myosin heavy chain IIb and SERCA1a) without elevated total protein T-nitration and S-nitrosylation. Thus, spaceflight affects SERCA function differently between the soleus and TA. This dataset derives results from the calcium uptake (spectrofluorometry) assay.*


Please use the files provided here as I have combined the two results into one CSV. 

Results: LSDS-13_calcium-uptake_fajardoTRANSFORMED_1_72_85_93.csv
Full sample information: OSD-488-samples.csv

LSDS-13_calcium-uptake_fajardoTRANSFORMED_1_72_85_93.csv contains the ratio of Ca2+-bound to Ca2+-free for the times (reported in 20 second intervals) 

## Read in the data

Read in the two files

&nbsp;

## F-test (1 point)

The aim of this study is to compare the Ca2+ uptake in samples taken from space flight to those in various control groups (Cohort_Control, Vivarium_Control, and Ground_Control). This is measured across various time points. 

One of the things we will want to know is if the variance is different between our samples.

### Question 1

Use the F-test to test equal variances at time-point twenty (20) between
- Space_Flight vs Ground Control
- Space_Flight vs Cohort_Control

Report the F-value and if there is a statistically significant difference in the variances. 

&nbsp;

## T-test - One Sample (1 point)

You are a researcher who conducted a similar experiment in tibialis samples and found a Ca2+ ratio with a mean of 0.8. You want to compare your results to the results in this study. To do that, you want to find the time point with a mean Ca2+ ratio that is _not_ statistically different from yours. 

### Question 2

At which time point(s) does the mean of all of the **tibialis** samples _not_ deviate significantly from 0.8?

&nbsp;

## T-Test - Two sample Tibialis (1 point)

The central aim of this study is to see the effect of space flight on Ca2+ ratio. Therefore, let's compare the mean Ca2+ ratios between tibialis in space flight and those on ground control. You decide to examine two time points - 20 and 480

### Question 2.1

First, use the F-Test to determine if the variances of the two samples at time points 20 and 480 are statistically different from 1. 

### Question 2.2 

Second, Use the two-sample t-test with either equal or unequal variances (based on your result above) to compare the means of Ca2+ ratios in the tibialis at times 20 and 480. Is there statistical support for a difference in Ca2+ ratios after space flight?


&nbsp;

## T-Test - Two Sample Soleus (1 point)

Repeat the above test using the soleus samples. You will again use the two time points (20 and 480) and compare space flight and ground control. 


### Question 3.1

First, use the F-Test to determine if the variances of the two samples at time points 20 and 480 are statistically different from 1. 

### Question 3.2 

Second, Use the two-sample t-test with either equal or unequal variances (based on your result above) to compare the means of Ca2+ ratios in the tibialis at times 20 and 480. Is there statistical support for a difference in Ca2+ ratios after space flight?

&nbsp;
&nbsp;

## Chi-Squared Test (2 points)

Someone in your lab was worried that the "Sample Preservation Method" (listed in the OSD-488-samples.csv) data was affecting the Ca2+ ratios in your soleus muscle samples - especially at later time points. 

Use the appropriate chi-squared test to test if there is a difference in the proportion of control mice (Cohort Control, Ground Control and Vivarium Control together) mice with a Ca2+ ration >=1 with the proportion of mice with a Ca2+ ratio < 1 that were processed in either RNALater or Liquid Nitrogen. Limit this to soleus muscle at the 480 time point.

### Question 4.1 

What is the p-value of your test?

### Question 4.2

Based on the results of this test (including any errors) what would you tell your labmate? 



## Additional hypotheses (4 points)

There are _many_ more hypotheses we could test with this data. Now you need to come up with a hypothesis to test! Complete the steps below (1 point each)
1. Write out a hypothesis/question to test.
2. Select the appropriate test and provide the null and alternative hypotheses.
3. Conduct the test
4. In 1-2 sentences summarize your results 

