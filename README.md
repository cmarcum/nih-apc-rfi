# nih-apc-rfi
A repository for responses to the NIH APC RFI NOT-OD-25-138

## About
This repository provides machine-readable access to comments submitted by the public in response to NIH NOT-OD-25-138, "Compiled Public Comments on the Request for Information on Maximizing Research Funds by Limiting Allowable Publishing Costs." The source of the data were originally published by NIH here: [https://osp.od.nih.gov/wp-content/uploads/2025/12/Compiled-Public-Comments-on-the-RFI-on-Maximizing-Research-Funds-by-Limiting-Allowable-Publishing-Costs.pdf](https://osp.od.nih.gov/wp-content/uploads/2025/12/Compiled-Public-Comments-on-the-RFI-on-Maximizing-Research-Funds-by-Limiting-Allowable-Publishing-Costs.pdf). 

The comments may contain proprietary, copyrighted, and personally identifiable information and the content is exclusively the responsibility of the author.

## Manifest
The three machine-readable formats are as follows:

nih.apc.csv - a comma-separated file.

nih.apc.json - a structured json object

nih.apc.rds - an R binary file containing an R data.frame object

All three file formats have the following features:
-  Record.ID - The numeric id of the comment from the source file.
-  Header.Title - The name associated with the comment. This could be an organization or individual.
-  Submit.Date - Date of submission.
-  Name - The name of the individual submitting the comment.
-  Organization - The name of the organization an individual may be affiliated with or submitting on behalf of.
-  Organization.Type - The type of the organization with values:
 -    [1] "Academic Institution"                                        
 -    [2] "Healthcare Industry (Biotech/Device/ Pharmaceutical Company)"
 -    [3] "Non-profit Research Organization"                            
 -    [4] "Not Applicable"                                              
 -    [5] "Other"                                                       
 -    [6] "Professional Organization/Association"                       
 -    [7] "Research Participant/Patient Advocacy Organization"          
 -    [8] "Scholarly Publisher/Journal"
-  Upload - The URL of any file uploaded with the submission. In the case of multiple files, only the first file was retained here.
-  Comment - The full comment. This field has been roughly cleaned to remove artifacts from conversion to ascii. If the submission had substantive responses to the five questions (see, Q1-Q5), then this field is               the concatenation of all of those responses. If the submission was entirely from an uploaded file, then this field contains only the extracted text from that file.
-  Upload.Description - Details about the nature of the uploaded file(s).
-  Q1 - Response to question 1: "Proposed Policy Options:" (Not cleaned/scrubbed)
-  Q2 - Response to question 2: "Available evidence related to publication costs and proposed options:" (Not cleaned/scrubbed)
-  Q3 - Response to question 3: "Peer review compensation:" (Not cleaned/scrubbed)
-  Q4 - Response to question 4: "Publishing best practices:" (Not cleaned/scrubbed)
-  Q5 - Response to question 5: "Other Comments:" (Not cleaned/scrubbed)

files/ - a directory of source materials, including uploaded files associated with a comment submission named consistent with their Record.ID
