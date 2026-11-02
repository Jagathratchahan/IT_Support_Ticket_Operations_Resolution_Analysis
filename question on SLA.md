-------QUESTION RELATED TO Service Level Agreement------

BUSINESS Problem:- 
  Identify tickets that do not comply with the  SLA and how to rectify them.
  
BUSINESS INSIGHT:-
 The dashboard helps the manager identify tickets that breached SLA compliance.


KEY CONCEPT:- What is a Service Level Agreement breach?

A failure to meet the  performance goals, response times, or uptime standards in a contract between a service provider and a customer.In this case, a resolution time violation.
Example: If a High-severity ticket takes 11 hours, then:

Target resolution time(Set by SLA policy) = 8 hours
Actual = 11 hours
SLA breach = Yes
Delay = 3 hours

-------------------- ADDITIONAL COLUMN ADDED APART FROM ACTUAL RAW DATA COLUMNS-----------------

Columns added are as follows:
  SLA Breach Flag (Column name) 
  DAX EXPRESSION - SLA Breach Flag = 
IF(
    'ticket_raw_data'[Resolution Time (Hrs)]
        > 'ticket_raw_data'[Target Resolution time],
    1,
    0
)

 SLA Status (Column name)
DAX EXPRESSION - SLA Status = 
IF(
    'ticket_raw_data'[Resolution Time (Hrs)]
        > 'ticket_raw_data'[Target Resolution Time],
    "Breach",
    "Within SLA"
)

SLA Breach % - DAX MEASURE
SLA Breach % = 
DIVIDE(
    SUM('ticket_raw_data'[SLA Breach Flag]),
    COUNTROWS('ticket_raw_data'),
    0
)

AVERAGE SLA Delay - DAX MEASURE
Average SLA Delay = 
AVERAGEX(
    FILTER(
        'ticket_raw_data',
        'ticket_raw_data'[SLA Breach Flag] = 1
    ),
    'ticket_raw_data'[Resolution Time (Hrs)]
        - 'ticket_raw_data'[Target resolution time]
)


--------------BUSINESS INSIGHT DASHBOARD--------------

The dashboard answers the following questions and provides much more insights

→ How serious is the SLA problem? 

→ Where is it happening? 

→ What severity/category drives it? 

→ Which individual tickets need attention?

<img width="1368" height="887" alt="Screenshot 2026-09-28 132432" src="https://github.com/user-attachments/assets/760ed3fc-2ce3-4189-a711-eb13b732a1e2" />




