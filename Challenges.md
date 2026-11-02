This document focuses on challenges, bottleneck identification,
resource allocation, severity vs. resolution, and root cause analysis.


1. Which ticket categories and regions have the highest average resolution times?

   It identifies slow operations.

<img src="Ticket Summary.png" alt="Alternative text" width="1000">


2. Resource Allocation

Where should we allocate additional support resources to reduce overall resolution time?

Identify where the combination of workload and slow resolution creates the biggest operational problem.

Workload → How many tickets are coming from each Region/Category?

Efficiency → How long does it take to resolve them?

<img src="Ticket Summary.png" alt="Alternative text" width="1000">

3. Severity vs. Resolution time

Do high-severity tickets actually receive faster resolution than lower-severity tickets?

<img src="Ticket Summary.png" alt="Alternative text" width="1000">



4. Root-Cause Analysis

What characteristics are most strongly associated with tickets taking unusually long to resolve?

The dataset cannot prove the actual root cause because it doesn't contain fields such as agent, issue complexity, number of escalations, downtime, or resolution type. Still, you can identify patterns/drivers associated with long resolution times.

A simple business definition is:

Long-resolution ticket = Resolution Time > Target Resolution Hrs

So your root-cause section can be:

Category → Severity → Region → SLA Breaches → Average Resolution Time

That gives you a strong path from "where is the problem?" → "what type of ticket?" → "where geographically?"
