This document focuses on challenges, bottleneck identification,
resource allocation, severity vs. resolution, and root cause analysis.


1. Which ticket categories and regions have the highest average resolution times?

   It provides insights into identifying where support operations are slow.

<img width="1368" height="887" alt="Screenshot 2026-09-28 132432" src="https://github.com/user-attachments/assets/e8d53408-a2ae-4614-bff7-c83f81eedca7" />


2. Resource Allocation

Where should we allocate additional support resources to reduce overall resolution time?

Identify where the combination of workload and slow resolution creates the biggest operational problem.

Workload → How many tickets are coming from each Region/Category?

Efficiency → How long does it take to resolve them?


<img width="1353" height="758" alt="Screenshot 2026-09-28 132548" src="https://github.com/user-attachments/assets/a6086b15-8c5e-4ac8-9ae8-08547f332090" />

3. Severity vs. Resolution time

Do high-severity tickets actually receive faster resolution than lower-severity tickets?

<img width="1353" height="758" alt="Screenshot 2026-09-28 132548" src="https://github.com/user-attachments/assets/f8aa2a1d-8a27-47d9-944c-5da8fc3558aa" />



4. Root-Cause Analysis

What characteristics are most strongly associated with tickets taking unusually long to resolve?

The dataset cannot prove the actual root cause because it doesn't contain fields such as agent, issue complexity, number of escalations, downtime, or resolution type. Still, you can identify patterns/drivers associated with long resolution times.

A simple business definition is:

Long-resolution ticket = Resolution Time > Target Resolution Hrs

So your root-cause section can be:

Category → Severity → Region → SLA Breaches → Average Resolution Time

That gives you a strong path from "where is the problem?" → "what type of ticket?" → "where geographically?"



<img width="1353" height="758" alt="Screenshot 2026-09-28 132548" src="https://github.com/user-attachments/assets/37caf94c-870f-4048-b3d7-a131dbb7ae3d" />



<img width="1368" height="887" alt="Screenshot 2026-09-28 132432" src="https://github.com/user-attachments/assets/c7fdd74a-b902-4263-a12f-7383f3feb562" />



