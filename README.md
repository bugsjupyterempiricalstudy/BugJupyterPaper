# Supplementary Material of "Bug Analysis in Jupyter Notebook Projects: An Empirical Study" paper

This repository includes all the collected and analyzed data for this study.

## Mined data
#### In the **rawdata** directory are 3 mining data from StackOverflow and GitHub.

 - raw_data_stack.csv: This CSV file contains all data from StackOverflow Posts about Jupyter. To extract this base, the following querie were used. 
 
```
select Id,PostTypeId,AcceptedAnswerId,ParentId,CreationDate,DeletionDate,Score,ViewCount,OwnerUserId,OwnerDisplayName,
LastEditorUserId,LastEditorDisplayName,LastEditDate,LastActivityDate,Tags,AnswerCount,CommentCount,FavoriteCount,
ClosedDate,CommunityOwnedDate,ContentLicense,Title
from Posts where Tags LIKE '%jupyter-notebook%' or Tags LIKE '%jupyter%' or Tags LIKE '%google-colaboratory%' or
Title LIKE '%jupyter-notebook%' or Title LIKE '%jupyter%' or Title LIKE '%google-colaboratory%'
```
https://data.stackexchange.com/stackoverflow/query/1541588/jupyternotebookbugs

 - raw_data_stack_p2.zip: This ZIP file contains the body and discussions of previous posts. To extract this base, the following query was used:

```
select Id,BodyPost,BodyAnswers,TextComments
from Posts where Tags LIKE '%jupyter-notebook%' or Tags LIKE '%jupyter%' or Tags LIKE '%google-colaboratory%' or
Title LIKE '%jupyter-notebook%' or Title LIKE '%jupyter%' or Title LIKE '%google-colaboratory%'
```

 - raw_data_git.csv: This CSV file contains all data from GitHub commits. To extract this base, the GitHub API were used.

## Analyzed dataset
#### Using Cohen's kappa coefficient to define inter-rater reliability, the authors manually ranked the two databases in terms of Bugs, Root Causes, and Impacts.

 - dataset_stack.csv: This CSV file contains all data from sorted StackOverflow posts.

 - dataset_git.csv: This CSV file contains all sorted GitHub commit data.

## Interviews
#### In the **interviews** directory, there is a file:

 - interview_model.pdf: This PDF file contains the questions asked in the interviews.

## Analysis results
#### In the **results** directory, there is a 2 files:

 - results_.xlsx: This XLSX file contains the values, calculations and graphs of the analyzed data.
 - taxonomy.pdf: This PDF file contains the taxonomy defined in this research. 

