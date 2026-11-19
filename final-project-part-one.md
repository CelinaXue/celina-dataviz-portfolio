| [home page](https://celinaxue.github.io/celina-dataviz-portfolio/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Before You Book: When to Fly Out of Pittsburgh

# Outline

My project will explore how historical flight records can help CMU students choose between departure options from Pittsburgh. Students traveling for school breaks, interviews, or other trips may want to understand how departure time relates to delays and cancellations before booking. I will begin with a familiar situation: choosing between flights to the same destination at different times. I will then introduce flight outcomes at Pittsburgh International Airport and compare departure windows across selected routes. Next, I will examine monthly patterns to see whether the differences remain consistent throughout the year. These comparisons will guide the story’s main findings and help readers understand which patterns are relevant to their own trips. The project will end with an interactive comparison that encourages students to check historical delay and cancellation rates for their route and weigh that information alongside their schedules and other travel needs.

## Initial sketches

The sketches will show how the story moves from a familiar booking decision to comparisons readers can use when choosing a flight from Pittsburgh. All chart marks and example values will be labeled as illustrative until the analysis is complete.

### Sketch 1: Opening booking choice

The opening will show the project title, a short introduction, and two example flights to the same destination with different departure times. The question above them will be: “Which flight would you choose?” This will introduce the challenge of choosing a flight that fits a student's schedule while considering historical reliability.

<img width="1600" height="1200" alt="sketch-01-opening" src="https://github.com/user-attachments/assets/5c5df2cf-00ac-4592-939d-07191048cb48" />


### Sketch 2: Flight outcomes

A 100% stacked bar will introduce the overall outcomes of scheduled PIT departures: on-time arrivals, arrivals delayed 15–59 minutes, arrivals delayed 60 minutes or more, cancellations, and diversions. These categories will be mutually exclusive. Records with insufficient information will be disclosed separately. This chart will establish the overall picture before the story moves into route-specific comparisons.

<img width="1600" height="1200" alt="sketch-02-outcomes" src="https://github.com/user-attachments/assets/9c67051c-2821-44e0-a3c5-3a4912efaf3b" />


### Sketch 3: Departure windows by route

Small multiple bar charts will compare arrival delay rates across departure windows for three selected destinations. The horizontal axis will show overnight, morning, afternoon, and evening departures. The vertical axis will show arrival delay rates, with the same scale across all route charts. Flight counts will appear alongside the comparisons, and cancellation rates will be shown separately.

<img width="1600" height="1200" alt="sketch-03-routes" src="https://github.com/user-attachments/assets/74fa5222-e8a1-489f-a1fb-00d25dbb8d73" />


### Sketch 4: Monthly patterns

A line chart will show monthly arrival delay rates for a selected route, with separate lines for each departure window. A destination selector will let readers explore whether the patterns differ across routes. Annotations will explain findings supported by the analysis, and groups with too few flights will be flagged.

<img width="1600" height="1200" alt="sketch-04-months" src="https://github.com/user-attachments/assets/3b5e239a-f9ae-4b1a-a098-2f8233d55faf" />


### Sketch 5: Airline comparison

This section will ask: “Which airline was more reliable on this route?” Two separate horizontal bar charts will compare arrival delay rates and cancellation rates among operating carriers serving the same destination. Readers will be able to select a route and departure window, and flight counts will appear beside the results. The section will explain that the operating carrier may differ from the airline brand shown when booking.

<img width="1600" height="1200" alt="sketch-05-airlines" src="https://github.com/user-attachments/assets/a4552ae3-360e-4c88-bf65-32d866f9bb26" />


### Sketch 6: Final interactive comparison

The final section will bring the comparisons together. Readers will select a destination and explore departure windows and operating carriers, with arrival delay rates, cancellation rates, and flight counts displayed separately. Short explanations will highlight the findings and their limitations. The story will end by encouraging readers to consider historical reliability alongside their schedule and other travel needs before booking.

<img width="1600" height="1200" alt="sketch-06-decision" src="https://github.com/user-attachments/assets/136ee13d-e905-4c6a-bae2-11ab0d4835dc" />


# The data

My primary source is the Bureau of Transportation Statistics (BTS) Reporting Carrier On-Time Performance dataset, which contains flight-level records for domestic flight segments operated by reporting carriers. I downloaded the monthly files for January through December 2025. Using Python and pandas, I filtered each file for flights departing Pittsburgh International Airport (`ORIGIN = PIT`) and combined the results into `pit_flights_2025.csv`. The combined dataset contains 43,176 flight records. It includes flight dates, operating carrier codes, destinations, scheduled departure times, arrival delays, cancellation and diversion indicators, and reported delay causes. I will use the official [BTS field descriptions](https://www.transtats.bts.gov/Fields.asp?gnoyr_VQ=FGJ) to interpret these variables.

I will group flights by scheduled departure time in Pittsburgh: overnight (00:00–05:59), morning (06:00–11:59), afternoon (12:00–17:59), and evening (18:00–23:59). I will calculate arrival delay rates among noncanceled, nondiverted flights with valid arrival information, and cancellation rates among all scheduled flights in each group. Following the [BTS definition](https://www.bts.gov/explore-topics-and-geography/topics/airline-time-performance-and-causes-flight-delays), an arrival delay of 15 minutes or more will count as late. I will select three destinations after checking flight counts and coverage across departure windows, then examine whether the patterns change across months.

I will also compare operating carriers on selected routes served by multiple airlines. I will show arrival delay rates, cancellation rates, and flight counts, and check whether differences remain within similar departure windows and months. Groups with limited observations will be flagged. The airline field in my file, `OP_UNIQUE_CARRIER`, identifies the operating carrier; the file does not include a marketing-carrier field, so these comparisons will be labeled accordingly. The analysis will describe historical reliability rather than overall airline quality. It will not establish that departure timing or airline choice causes delays, predict an individual flight's outcome, or assess ticket prices, comfort, or connection success.
<img width="1600" height="1200" alt="sketch-01-opening" src="https://github.com/user-attachments/assets/23d0b004-7ebf-45ba-8c6a-923907634ea9" />

**Working data status:** The public source has been identified. The 2025 PIT working dataset still needs to be downloaded, checked, and made available through a public link before submission.

| Name | URL | Description |
|------|-----|-------------|
| BTS Reporting Carrier On-Time Performance | [Official data directory](https://www.transtats.bts.gov/PREZIP/) | I have downloaded the January–December 2025 monthly files from this directory. I will use records with Pittsburgh International Airport (`PIT`) as the origin. |

# Method and medium

I plan to use Python and pandas to filter, check, and summarize the flight records. I will create the visualizations in Tableau and use Shorthand to combine the charts with short explanations in an interactive story. My GitHub portfolio will document the proposal, sketches, data sources, and later project updates. During later development, I will ask students to review the story and use their feedback to improve its clarity and usefulness.

## References

- Bureau of Transportation Statistics. (n.d.). *Reporting Carrier On-Time Performance (1987–present): Field descriptions and download access.* U.S. Department of Transportation. https://www.transtats.bts.gov/Fields.asp?gnoyr_VQ=FGJ
- Bureau of Transportation Statistics. (n.d.). *Airline on-time statistics.* U.S. Department of Transportation. https://www.transtats.bts.gov/ONTIME/
- Bureau of Transportation Statistics. (2021, March 16). *Airline on-time performance and causes of flight delays.* U.S. Department of Transportation. https://www.bts.gov/explore-topics-and-geography/topics/airline-time-performance-and-causes-flight-delays

## AI acknowledgements

I used ChatGPT to identify possible public data sources.
