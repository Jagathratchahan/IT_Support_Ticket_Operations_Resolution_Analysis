This document helps us to find other business-related questions apart from SLA, such as bottleneck identification,
resource allocation, severity vs resolution, root cause analysis.


1. Which ticket categories and regions have the highest average resolution times?

   It provides insights into identifying where support operations are slow.

   
<img width="1868" height="911" alt="image" src="https://github.com/user-attachments/assets/01b2f2e8-02ea-4534-b88a-d19118324aa1" />


2. Resource Allocation

Where should we allocate additional support resources to reduce overall resolution time?

KEY CONCEPT:- 

You need to identify where the combination of workload + slow resolution creates the biggest operational problem.

Workload → How many tickets are coming from each Region/Category?

Efficiency → How long does it take to resolve them?


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9bd2dd50-e9b8-483d-a156-911872ab8d97" />


3. Severity vs. Resolution time

Do high-severity tickets actually receive faster resolution than lower-severity tickets?

<img width="1920" height="897" alt="image" src="https://github.com/user-attachments/assets/9b746a93-81e9-451a-ab02-e62fc3c17863" />


4. Root-Cause Analysis

What characteristics are most strongly associated with tickets taking unusually long to resolve?

The current dataset cannot prove the actual root cause because it doesn't contain fields such as agent, issue complexity, number of escalations, downtime, or resolution type 
But you can identify patterns/drivers associated with long resolution times.

A simple business definition is:

Long-resolution ticket = Resolution Time > Target Resolution Hrs

So your root-cause section can be:

Category → Severity → Region → SLA Breaches → Average Resolution Time

That gives you a strong path from "where is the problem?" → "what type of ticket?" → "where geographically?".


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/40b75675-43b2-4d09-8311-2b4ffec3a9de" />
