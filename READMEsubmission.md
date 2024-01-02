# Maine-Focused Standardized Testing Guidance Project

## Data Used

act2019 - List of ACT information by state in 2019\
sat2019 - List of SAT information by state in 2019\
sat_act_by_college - Information relating SAT and ACT scores to college admissions\
collegescorecard2019locationinfo - Location information from colleges, derived from pulling location information from 2019 College Scorecard (https://collegescorecard.ed.gov/data/) \
satact2019 - Merged dataset derived from act2019 and sat2019\
satactbycollegewithlocation - Merged dataset derived from sat_act_by_college and collegescorecard2019locationinfo

## Problem Statement

As a high school guidance counselor in the state of Maine, I have observed trends in SAT and ACT score requirements by various colleges--in state and out of state--that my students have expressed interest in. I need to use this information to help guide them toward achieveable institutions that are the best fit for them, both academically and personally.

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
|sat_total_25th_percentile|object|satactbycollegewithlocation|This is the 25th percentile value for SAT scores of accepted students at the institution|
|sat_total_75th_percentile|object|satactbycollegewithlocation|This is the 75th percentile value for SAT scores of accepted students at the institution|
|act_total_25th_percentile|object|satactbycollegewithlocation|This is the 25th percentile value for ACT scores of accepted students at the institution|
|act_total_75th_percentile|object|satactbycollegewithlocation|This is the 75th percentile value for ACT scores of accepted students at the institution|

## Summary of Analysis

The code for this project contains the addition of several new variables derived from data already included in the provided datasets, with the exception of location information for unversities. The analysis focused on the thresholds for standardized test scores that colleges and universities in the U.S. see within their student population and how those scores were distributed among different states, with a significant focus on the state of Maine. 

## Conclusions and Recommendations Based on Problem Statement

The information gathered would be helpful in advising a student that is looking at applying to colleges and universities. Even with the beginning of a shift away from standardized testing as an educational performance benchmark, it is still plain to see that students will benefit from raising test scores. That being said, the observation that some universities are now permanently test-optional can be reassuring for students that may not test well for a variety of reasons, such as learning disabilities and test anxieties. Overall, while I would still recommend prepping for and taking standardized tests, I would also recommend not sacrificing well-being for them if a student is looking into schools that may not weigh the results as much. In particular, this seems to be the case with schools in Maine, where my student population would be located, and in a growing number of schools around the country.