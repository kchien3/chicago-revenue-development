# City of Chicago Parking Tickets
## Data Exploration and Revenue Development Strategies


### Background and Motivation
The City of Chicago has a long history of corruption dating back over 150 years.(source) A 2019 report by the Illinois Policy Institute estimated that public corruption convictions cost the Illinois state economy $9.9 billion between 2000-2017, with further detrimental effects on economic competitiveness and growth. (source) In order to maintain its reputation as the most corrupt city in America, Chicago must explore ways to unlock the full potential of its municipal revenue streams.

### Data Description
ProPublica, an investigative journalism organization, has compiled a data set of parking and vehicle compliance tickets issued in Chicago from January 1, 1996 to May 14, 2018. The same data are available from the City of Chicago through FOIA (Free of Information Act) requests. In addition to the 22 features provided by the City of Chicago, ProPublica also engineered 14 additional features containing geographic information about where the ticket was issued. ProPublica also compiled a data set of speeding and red light camera violation tickets in a separate csv but I did not use that data in this project.

At a high level, the data set contains information about when, where, and by whom tickets were issued, hashed license plate numbers, vehicle makes, vehicle registration zipcodes, the violation for which the vehicle was cited, payment status and more.

### Data Pipeline
The uncompressed csv containing the data is 19.6 GB and contains 54,430,547 records, far too large to load completely into a single computer's memory. I used Unix commands to systematically sample every 25th record, producing a subset containing 2,177,221 records that consumed 650 MB in memory. The pandas software library was used to examine, plot and analyze this subset of data.

### Data Exploration
This section contains plots that demonstrate the types of information that can be gleaned from this feature-rich data set.

#### Tickets Issued by Year and Fines Paid by Year
![png](img/tickets_by_year.png)
what data do i have?
speeding/red light tickets data (not used)
parking/parked car violations (used)

what options does the city have?
where to send enforcement agents
the price to set tickets

(can compare the ticket writing numbers for different officers)
(can plot the area an officer works)
(maybe can measure the performance of different agencies)

what kind of violations are there?
what violations make the most money?


5 figures + title slide (3 slides of eda. 2 slides of hypothesis testing)
1 introduction to data set
systematic sample

2 overview of data set
3 highest sources of revenue ytd 5/14/18 (parking data only) (top 5, then top 10 if time allows)

|   Code   |               Violation Description               | FY2019 Revenue |
|:--------:|:-------------------------------------------------:|:--------------:|
| 0964125B | No city sticker vehicle under/equal to 16,000 lbs | \$924,032.51    |
| 0964040B | Street cleaning                                   | \$544,842.56    |
| 0964090E | Residential permit parking                        | \$501,186.09    |
| 0964190A | Exp. meter non-central business district          | \$411,177.41    |
| 0964150B | Parking/standing prohibited anytime               | \$338,213.08    |

4 does raising ticket price affect probability of payment? (pick violations with highest ticket prices and price increases)
5 does raising ticket price affect number of tickets issued?
6 which violations burden non-poor minorities (in areas without a lot of political fundraising too)
7 which non law enforcement departments perform well? show individual officer data.
8 future direction
