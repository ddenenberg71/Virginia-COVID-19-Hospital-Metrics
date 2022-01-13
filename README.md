# Overview

Data gleaned daily, by David Denenberg, from the Virginia Hospital & Healthcare Association "COVID-19 in Virginia Hospitals" dashboard at https://www.vhha.com/communications/virginia-hospital-covid-19-data-dashboard/. View this data in chart form at http://covid19va.net.

# Notice

You are free to reuse this data.  This repository is **not** affiliated with the Virginia Hospital & Healthcare Association (VHHA) or the Virginia Department of Health (VDH).

# Ongoing Advisories
- 2022-01-12: The VHHA added two fields to the dashboard today: "Inpatient Staffed Beds - Non-ICU Beds Available (Adult)" and "Inpatient Staffed Beds - ICU Beds Available (Adult)"

# Files

- vhhaCovid19HospitalMetrics.csv: Statistics updated daily by the VHHA.
- vhhaCovid19Vaccinations.csv: Vaccination statistic updated weekly by the VHHA. 

# Fields in vhhaCovid19HospitalMetrics.csv
Explanations appearing in quotes come directly from the VHHA COVID-19 dashboard.  An empty/missing value usually indicates the VHHA had not yet added the item to the dashboard as of the date indicated. 

- date: YYYY-MM-DD format.  "As of" date from the dashboard.
- hospitalized: Integer. "Combined number of confirmed positive COVID-19 patients who are currently hospitalized, and hospitalized patients whose COVID-19 test results are pending.
- hospitalizedConfirmed: Integer. "Total number of currently hospitalized patients confirmed positive for COVID-19."
- hospitalizedIcu: Integer. "Combined number of confirmed positive COVID-19 patients, and those whose COVID-19 test results are pending, currently hospitalized in the ICU."
- hospitalizedTestResultsPending: Integer. "Total number of people currently receiving inpatient hospital care whose COVID-19 test results are pending."
- hospitalizedVentilator: Integer. "Combined number of hospital patients, both confirmed for COVID-19, and those with test results pending, currently on a ventilator." The VHHA stopped reporting this statistic as of July 23, 2021.
- ventilatorsOnHand: Integer. "Total ventilators on-hand in hospitals." The VHHA stopped reporting this statistic as of July 23, 2021.
- ventilatorsInUse: Integer. "Total ventilators in use at hospitals." The VHHA stopped reporting this statistic as of July 23, 2021.
- ventilatorsUtilization: Decimal (representing a percentage).  "Share of total ventilators in use." The VHHA stopped reporting this statistic as of July 23, 2021.
- bedAvailability: Integer. "Inpatient Staffed Beds - Total available beds." The VHHA stopped did not publish this statistic from July 23, 2021 through September 1, 2021.
- hospitalsPpeDifficulty: Integer. "Number of Virginia hospitals experiencing difficulty in obtaining or replenishing PPE in the next 72 hours." The VHHA stopped reporting this statistic as of July 23, 2021.
- hospitalsOtherDifficulty: Integer. "Number of Virginia hospitals experiencing difficulty in obtaining or replenishing other medical supplies in the next 72 hours." The VHHA stopped reporting this statistic as of July 23, 2021.
- discharged: Integer. "The total number of confirmed COVID-19 patients who have been hospitalized and discharged."
- icuOccupancy: Decimal (representing a percentage). "ICU Occupancy" and "Current total ICU bed occupancy in Virginia hospitals, including COVID-19 and non-COVID patients."  This comment also applies to the next two statistics. The VHHA stopped reporting this statistic as of July 23, 2021.
- icuSurgeBeds: Integer. "ICU Surge Beds." The VHHA stopped reporting this statistic as of July 23, 2021.
- icuSurgeOccupancy: Decimal (representing a percentage). "ICU Occupancy including Surge Beds".  The VHHA stopped reporting this statistic as of July 23, 2021.
- totalNonIcuBedsAvailable: Integer. "Inpatient Staffed Beds - Total non-ICU beds available (Adult and Pediatric)".  The VHHA started reporting this on September 2, 2021.
- totalIcuBedsAvailable: Integer. "Inpatient Staffed Beds - Total ICU beds available (Adult and Pediatric)".  The VHHA started reporting this on September 2, 2021.
- nonIcuBedsAvailableAdultOnly: Integer. "Inpatient Staffed Beds - Non-ICU Beds Available (Adult)". The VHHA started reporting this on January 12, 2022. 
- icuBedsAvailableAdultOnly: Integer. "Inpatient Staffed Beds - ICU Beds Available (Adult)". The VHHA started reporting this on January 12, 2022.

# Fields in vhhaCovid19Vaccinations.csv
Explanations appearing in quotes come directly from the VHHA COVID-19 dashboard.  NOTE: The VHHA stopped updating this statistic after May 20, 2021 and removed it from the VHHA COVID-19 dashboard on July 23, 2021.

- date: YYYY-MM-DD format.  "Administered as of" date as reported in the dashboard.
- totalHospitalVaccinations: Integer. "COVID-19 Vaccines Administered by Hospitals. Weekly tally of COVID-19 vaccine doses administered by Virginia hospitals and health systems."  The "weekly tally" explanation from the VHHA is a bit confusing.  This number is, indeed, an inception-to-date cumulative count of COVID-19 vaccinations.

# Observations
Various observations of data published in the VHHA Dashboard.

- 2021-09-03: When the VHHA published the dashboard on July 6, 2021 the Bed Availability statistic appears to have been double-counted (or something like that).  It was published as 6,885.  On July 4 it was published as 3,602.  No dashboard was published on July 5.  On July 7 it was published as 3,533.  Working under the assumption 6,885 was an error, this value is omitted from the data for July 6.  It appears to be a safe assumption the actual value would have been in the 3,400-3,600 range.  
- 2021-09-03: Two fields were added to this dataset reflect the new ICU/non-ICU Bed Availability statistics published on the VHHA dashboard starting September 2, 2021.
- 2021-09-02: The VHHA resumed reporting bed availability statistics today, but differently than before.  A new "Inpatient Beds - Total Available Beds" statistic aligns with their prior total available beds statistic thus is now captured in the same "bedAvailability" field.  The two other new fields (Total ICU Beds, Total non-ICU Beds) don't align with their older statistics so new fields will probably be added to this file to capture those statistics in the next day or two.    
- 2021-07-24: On July 23, the VHHA stopped publishing 10 of the daily hospital metrics and the occasional hospital vaccination metric. 
- 2021-07-05: The VHHA did not update the dashboard for July 5, 2021.
- 2021-07-01: The VHHA did not update the dashboard for July 1, 2021.
- 2021-03-13: The VHHA corrected the 114 to 1 for the error observed yesterday.  
- 2021-03-12: Today the VHHA dashboard showed a count of 114 for "Number of Virginia hospitals experiencing difficulty in obtaining or replenishing other medical supplies in the next 72 hours."  I am assuming this is a typo.  Since early April 2020, this number has never exceed 3.  It's only ever been non-zero about 35 times in the last ~340 days and hasn't been greater than 1 since mid-April 2020.  For now, I recorded the observed 114 as zero, but will correct it if it becomes clear there is, indeed, some sudden and pervasive supply challenge. 
- 2020-12-28: On this day the dashboard showed a count of ICU Surge Beds of 1,269 even though the prior day showed 869 and the next day showed 850.  This was likely a typo from the VHHA.