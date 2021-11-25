The DEBAGREEMENT is subdivided into three folders. 


RAW: contains raw comments data, divided into separate CSVs by subreddit from which they were scraped. The columns are as follows: 
- author: the username of the author who wrote the comment
- body: the text body of the comment
- created_utc: timestamp in UNIX time of when comment was created
- id: comment's unique ID 
- parent_id: unique ID of either comment or submission to which comment responds
- submission_id: unique ID of submission on which comment was made


LABELED DATASET: contains all comment interactions, labeled as either 0- disagree, 1- neutral, 2- agree, where 66% or 2/3 agreement is reached among annotators on the label 
UNSURE LABELS:  contains all comment interactions where either annotators had lower than 66% or 2/3 agreement on the final label or the interaction was labeled as -100 - unsure by a majority of annotators. 

The columns for both datasets are as follows: 
msg_id_parent: the reddit identifier for the parent message
msg_id_child: the reddit identifier for the child message
submission_id: the reddit identifier for the submission
body_parent: the text of the parent comment
body_child: the text of the child comment
submission_text: abbreviated submission text
subreddit: subreddit name on which the interaction took place
author_parent: reddit username of parent author
exact_time: UTC timestamp of time when interaction occurred
author_child: reddit username of child author
datetime: datetime timestamp  for  when  interaction  occurred,  formatted  as  YYYY-MM-DD HH:MM:SS
agreement_fraction: the fraction of annotators that agree with the final label
individual_kappa: the Fleiss’ kappa for each annotation. Calculation of Fleiss’ kappa is taken from appendix A.2 of paper by S. Chen, D. Khashabi, W. Yin, C. Callison-Burch, and D. Roth titled "Seeing things from a different angle: Discovering diverse perspectives about claims"