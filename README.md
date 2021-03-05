# Overview

Data gleaned daily, by David Denenberg, from the Virginia Hospital & Healthcare Association "COVID-19 in Virginia Hospitals" dashboard at https://www.vhha.com/communications/virginia-hospital-covid-19-data-dashboard/. View this data in chart form at http://covid19va.net.

# Notice

You are free to reuse this data.  This repository is **not** affiliated with the Virginia Hospital & Healthcare Association (VHHA) or the Virginia Department of Health (VDH).

# Advisories

- No advisories.

# Files

- vhhaCovid19HospitalMetrics.csv: Statistics updated daily by the VHHA.
- vhhaCovid19Vaccinations.csv: Vaccination statistic updated weekly by the VHHA. 

# Fields in vhhaCovid19HospitalMetrics.csv
Explanations appearing in quotes come directly from the VHHA COVID-19 dashboard (as it appeared on December 26, 2020).  An empty/missing value usually indicates the VHHA had not yet added the item to the dashboard as of the date indicated. 

- date: YYYY-MM-DD format.  "As of" date from the dashboard.
- hospitalized: Integer. "Combined number of confirmed positive COVID-19 patients who are currently hospitalized, and hospitalized patients whose COVID-19 test results are pending.
- hospitalizedConfirmed: Integer. "Total number of currently hospitalized patients confirmed positive for COVID-19."
- hospitalizedIcu: Integer. "Combined number of confirmed positive COVID-19 patients, and those whose COVID-19 test results are pending, currently hospitalized in the ICU."
- hospitalizedTestResultsPending: Integer. "Total number of people currently receiving inpatient hospital care whose COVID-19 test results are pending."
- hospitalizedVentilator: Integer. "Combined number of hospital patients, both confirmed for COVID-19, and those with test results pending, currently on a ventilator."
- ventilatorsOnHand: Integer. "Total ventilators on-hand in hospitals."
- ventilatorsInUse: Integer. "Total ventilators in use at hospitals."
- ventilatorsUtilization: Decimal (representing a percentage).  "Share of total ventilators in use."
- bedAvailability: Integer. "Inpatient bed availability"
- hospitalsPpeDifficulty: Integer. "Number of Virginia hospitals experiencing difficulty in obtaining or replenishing PPE in the next 72 hours."
- hospitalsOtherDifficulty: Integer. "Number of Virginia hospitals experiencing difficulty in obtaining or replenishing other medical supplies in the next 72 hours."
- discharged: Integer. "The total number of confirmed COVID-19 patients who have been hospitalized and discharged."
- icuOccupancy: Decimal (representing a percentage). "ICU Occupancy" and "Current total ICU bed occupancy in Virginia hospitals, including COVID-19 and non-COVID patients."  This comment also applies to the next two statistics.
- icuSurgeBeds: Integer. "ICU Surge Beds"
- icuSurgeOccupancy: Decimal (representing a percentage). "ICU Occupancy including Surge Beds". 

# Fields in vhhaCovid19Vaccinations.csv
Explanations appearing in quotes come directly from the VHHA COVID-19 dashboard

- date: YYYY-MM-DD format.  "Administered as of" date as reported in the dashboard.
- totalHospitalVaccinations: Integer. "COVID-19 Vaccines Administered by Hospitals. Weekly tally of COVID-19 vaccine doses administered by Virginia hospitals and health systems."  The "weekly tally" explanation from the VHHA is a bit confusing.  This number is, indeed, an inception-to-date cumulative count of COVID-19 vaccinations.

# Observations
Various observations of data published in the VHHA Dashboard.

- 2020-12-28: On this day the dashboard showed a count of ICU Surge Beds of 1,269 even though the prior day showed 869 and the next day showed 850.  This was likely a typo from the VHHA.