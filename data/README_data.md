# Data Directory

## Dataset: _RIT_Opportunity_Wise_Dataset.xlsx

The raw dataset used in this project is proprietary to Excelerate and cannot be shared publicly.

### Dataset Overview

| Property | Value |
|----------|-------|
| Total Records | 8,558 |
| Columns | 17 original + 10 engineered = 27 total |
| Opportunities | 22 unique |
| Categories | Internship, Course, Event, Competition, Engagement |
| Countries | 71 |
| Date Range | 2022–2024 |

### Original Columns

| Column | Type | Description |
|--------|------|-------------|
| Learner SignUp DateTime | Datetime | When the student registered on the platform |
| First Name | String | Student first name |
| Date of Birth | Date | Used to derive Age |
| Gender | Categorical | Male / Female / Other / Prefer not to say |
| Country | String | Student's country (71 unique values) |
| Institution Name | String | University/college |
| Current/Intended Major | String | Field of study |
| Opportunity Id | String | Unique ID for each opportunity |
| Opportunity Name | String | Name of the program |
| Category | Categorical | Internship / Course / Event / Competition / Engagement |
| Opportunity Start Date | Date | 54% missing |
| Opportunity End Date | Date | Program end date |
| Apply Date | Date | When student submitted their application |
| Status | Categorical | 8 statuses (Team Allocated, Started, Rejected, etc.) |
| Status Code | String | Coded version of Status |
| Status Description | String | Full description of status |
| Entry created at | Datetime | System timestamp |

### Engineered Features (Week 2)

| Feature | Description |
|---------|-------------|
| Age | Years between DOB and Nov 3, 2024 (clipped 15–65) |
| Age_Group | Bins: Under 18 / 18–22 / 23–26 / 27–30 / 30+ |
| Days_to_Apply | Days between signup and application (clipped ≥0) |
| SignUp_Month | Month of signup (1–12) |
| SignUp_Year | Year of signup |
| SignUp_Quarter | Quarter of signup (Q1–Q4) |
| Has_Start_Date | Binary: 1 if Start Date present, else 0 |
| Is_Placed | Binary target: 1 if Team Allocated/Started/Rewards Award |
| Country_Group | Top 5 countries + 'Other' |
| Gender_Clean | Standardized gender categories |

### Target Variable

`Is_Placed` = 1 if Status is **Team Allocated**, **Started**, or **Rewards Award**  
`Is_Placed` = 0 for all other statuses (Rejected, Dropped Out, Waitlisted, etc.)

**Class Balance:** 47.6% positive (4,072) | 52.4% negative (4,486)
