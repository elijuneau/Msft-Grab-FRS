# Introduction

Dear students, this document target to be the Q & A panel for all questions raised to Grab & Microsoft data science supporting team. 
During the check-in session on 1st October, the most common questions have been answered and listed below. 
If you have and other questions, please add it below following the format template:
- Qx: TBC [Submitter] [Date]

# Topics: 

## Traffic Management

Q1: What does the actual term for the 'demand' column? (as it's in a normalized form)
A1: The demand is normalized into scale of [0,1]. It indicates how many trips requested by passengers generated in this geospatial zone (geohash level 6) at certain time period

Q2: What does the 'day' column mean?
A2: The 'day' column shows the sequential order of the date among the time period for the dataset. (The dataset shows 2 month demand records, so the day is from 1 to 60)

Q3: Which region is the dataset targeting? in Southeast Asia? Do we have to find out on our own?
A3: The geohash area is not a real location in Southeast Asia. The geohash is more like a feature to classify the trip pattern for different zones.

Q4: Which country is the 'timestamp' column referring to? Based in Singapore? Or based on the Geohash location/country time zone?
A4: The timezone will not affect model building and performance, so to simplify, we may consider it as based in SG. 
The purpose of 'timestamp' is to cut the demand into 15 min interval time for the participants to identify the travel pattern change over the time.

## Safety

Q1: There are some duplicate data: Over unique booking 20000, 18 are duplicated. How should we handle these records?
A1: Checking whether there are duplicate records is a part of data cleaning step. If the label is incorrect, it's recommended to delete the records. 

Q1: The model accuracy for training data is 1.0, is it suppose to be correct?
A1: Model accuracy: 1.0 shall not be true, the reason might be overfitting or using un-balanced dataset. 
Student are suggest to figure out the reason through some exploration and you may record all the exploration process as script comments or included in the presentation slides. 

