# STS Matching

A small repository to match student preferences for thesis topics and availability of supervisors for a fair workload: Student Thesis Supervisor (STS) Matching.

The repository has two Jupyter notebooks. First is a web-crawler specifically for the GRS group at Wageningen University to prepare the list of supervisors and topics. The crawler works with the 2024 version of https://www.wur.nl. It may be necessary to update it if the website changes.

The second notebook is generic and can be used to solve the assignment problems between topics, student choices and supervisors. The code can process up to 3 topic preferences per student. There are 3 dummy csv files that demonstrate how the data needs to be formatted. 

The assignment is solved with a greedy algorithm that uses random data exploration to find a locally optimal assignment. The criteria are:

1. Topic is still available
    1. Topic has capacity to accommodate more students
    2. Supervisor has capacity to accommodate more students
    3. Cosupervisor - if present - has capacity to accommodate more students
2. Highest possible student preference

Often, the algorithm will not find a full assignment. The best runs are stored with a user provided cut-off. The candidate for best possible assignment can be exported at the end.