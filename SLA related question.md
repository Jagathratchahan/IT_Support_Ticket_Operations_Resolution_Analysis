-------QUESTION RELATED TO Service Level Agreement------

BUSINESS QUESTION:- 
  Are customer tickets resolved within the SLA target resolution time? If not, where are the SLA breaches occurring?
  
BUSINESS INSIGHT:-
 The dashboard helps the manager focus on where to resolve and inform customers when the problem is fixed.


KEY CONCEPT:- What is a Service Level Agreement breach?

A failure to meet the agreed-upon performance goals, response times, or uptime standards set in a contract between a service provider and a customer.In this case, a resolution time violation.
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


<img width="1874" height="925" alt="image" src="https://github.com/user-attachments/assets/938a4076-6b31-447e-8cce-46008b173c72" />



