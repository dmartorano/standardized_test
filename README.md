# Maine-Focused Standardized Testing Guidance Project

## Data Used

act2019 - List of ACT information by state in 2019\
sat2019 - List of SAT information by state in 2019\
sat_act_by_college - Information relating SAT and ACT scores to college admissions\
collegescorecard2019locationinfo - Location information from colleges, derived from pulling location information from 2019 College Scorecard (https://collegescorecard.ed.gov/data/) \
satact2019 - Merged dataset derived from act2019 and sat2019\
satactbycollegewithlocation - Merged dataset derived from sat_act_by_college and collegescorecard2019locationinfo

## Problem Statement

As a high school guidance counselor in the state of Maine, I have observed trends in SAT and ACT score requirements by various colleges--in state and out of state--that my students have expressed interest in. Namely, I have found that, in order for an institution to admit someone (based on test scores), a student generally needs to meet or exceed the average test score of the institution. I need to use this information to help guide them on whether they should submit test scores to test-optional institutions that are the best fit for them, both academically and personally.

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|satact2019|This is the two-letter abbreviation of the U.S. state where participation and scores are being tracked|
|sat_participation|object|satact2019|This is the participation rate by state for the SAT as a percent|
|readingwriting|int|satact2019|This is the average reading and writing SAT score for the state|
|math|int|satact2019|This is the average math SAT score for the state|
|total|int|satact2019|This is the average total SAT score for the state|
|act_participation|object|satact2019|This is the participation rate by state for the ACT as a percent|
|composite|float|satact2019|This is the average ACT composite score for the state|
|sat_participation_float|float|satact2019|This is the SAT participation rate as a float value|
|act_participation_float|float|satact2019|This is the ACT participation rate as a float value|
|school|object|satactbycollegewithlocation|This is the name of the post-secondary institution|
|test_optional|object|satactbycollegewithlocation|This states whether the institution requires the SAT/ACT|
|applies_to_class_year|object|satactbycollegewithlocation|This states what graduation year the test-optional policy applies to|
|policy_details|object|satactbycollegewithlocation|This includes specific details about the test-optional policy|
|number_of_applicants|int|satactbycollegewithlocation|This displays how many individuals applied to the institution|
|accept_rate|object|satactbycollegewithlocation|This is the rate at which students were accepted based on how many applied|
|sat_total_middle50_percentile|object|satactbycollegewithlocation|This is the 25-75 percentile range for the SAT score at the institution|
|act_total_middle50_percentile|object|satactbycollegewithlocation|This is the 25-75 percentile range for the ACT score at the institution|
|state|object|satactbycollegewithlocation|This shows in what state the institution is located|
|accept_rate_float|float|satactbycollegewithlocation|This is the acceptance rate of the institution as a float value|
|sat_total_25th_percentile|float|satactbycollegewithlocation|This is the 25th percentile value for SAT scores of accepted students at the institution|
|sat_total_75th_percentile|float|satactbycollegewithlocation|This is the 75th percentile value for SAT scores of accepted students at the institution|
|sat_school_avg|float|satactbycollegewithlocation|This is the average SAT score for this institution|
|act_total_25th_percentile|float|satactbycollegewithlocation|This is the 25th percentile value for ACT scores of accepted students at the institution|
|act_total_75th_percentile|float|satactbycollegewithlocation|This is the 75th percentile value for ACT scores of accepted students at the institution|
|act_school_avg|float|satactbycollegewithlocation|This is the average ACT score for this institution|
|should_scores_be_submitted|bool|satactbycollegewithlocation|This boolean determines whether, based on average Maine test scores, the institution may accept a Maine student|

## Summary of Analysis

The code for this project contains the addition of several new variables derived from data already included in the provided datasets, with the exception of location information for unversities. The analysis focused on the thresholds for standardized test scores that colleges and universities in the U.S. see within their student population and how those scores were distributed among different states, with a significant focus on the state of Maine. Specifically, this analysis is meant to help Maine students determine when and when not to submit their standardized test scores when optional.

## Conclusions and Recommendations Based on Problem Statement

The information gathered here would be helpful in advising a student that is looking at applying to colleges and universities. This biggest question that can be answered from the data provided is whether or not an average Maine student should submit their standardized test scores when they are given the option of not submitting them. Based on the data, the Maine test averages do not meet or exceed the average test scores of any institution within the dataset provided. This isn't to say that Maine students should not submit their test scores when applying to higher ed institutions if they perform somewhere above the average. What this information does say is that, on average, a Maine student may be better off omitting their standardized test scores if given the opportunity during the college application process.