# Pinnacle Ventures Aviation Risk Analysis

## Project Overview

**Pinnacle Ventures** is expanding into new industries and is interested in purchasing and operating airplanes for both commercial and private enterprises. However, the company lacks knowledge about the potential risks associated with different aircraft types. This analysis aims to determine which aircraft models are the lowest risk and provide actionable insights to guide purchasing decisions for the head of the new aviation division.

---

## Data Description

The dataset used in this analysis comes from the **National Transportation Safety Board (NTSB)** and includes aviation accident and incident data from 1962 to 2023. The key fields used in this analysis are:

- **Make**: Aircraft manufacturer 
- **Model**: Specific model of the aircraft 
- **Injury.Severity**: Classification of the incident outcome
- **Total.Fatal.Injuries**: Number of fatalities
- **Total.Serious.Injuries**: Number of serious injuries
- **Total.Minor.Injuries**: Number of minor injuries
- **Total.Uninjured**: Number of uninjured passengers
- **Aircraft.damage**: Extent of damage 
- **Purpose.of.flight**: Purpose of flight

---

## Data Preparation

1. **Select Relevant Columns**: Focus on the fields mentioned above to evaluate risk.
2. **Handle Missing Values**: 
   - Filled categorical fields with `'unknown'`.
   - Filled numeric fields with `0`.
3. **Standardize Text**: Converted all categorical text to lowercase.
4. **Feature Engineering**:
   - Created a combined **Make_Model** identifier for better categorization.

---

## Analysis Steps

1. **Injury-based Summary**:
   - Grouped by **Make** and **Model**, and calculated:
     - Total incidents (count)
     - Total fatalities (sum)
     - Most common severity (mode)
     - Total serious, minor, and uninjured counts
     
2. **Damage & Purpose Summary**:
   - Grouped by **Make** and **Model**, and extracted:
     - Most common damage type
     - Most common purpose of flight

3. **Identifying Low-risk Aircraft**:
   - Ranked models by **lowest fatalities** and **lowest severe damage** (substantial/destroyed).
   - Combined these rankings to highlight the safest candidates.



