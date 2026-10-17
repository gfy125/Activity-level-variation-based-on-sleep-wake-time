# 2025-DATA3406-CC06-Group4

# Introduction
- **Driving Question**: Do they show variation in activity levels depending on their sleep/wake times or late-night activity?
- **Importance**: Understanding how sleep and wake patterns influence daily activity levels is crucial for promoting healthier lifestyles and improving wellbeing. By analysing wearable fitness data, we can identify whether irregular sleep habits or late-night activity affect overall physical performance. These insights can inform personalized health recommendations, support healthcare education, and guide the design of digital health tools that encourage balanced daily routines.

# Team Members & Roles
 - [Alan Shih](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki/Alan-Personal-Planning-and-Progress)
 - [Fengyuan Guo](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki/Fengyuan-Guo-%E2%80%90-Personal-Planning-and-Progress)
 - [Man Hei Lee](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki/Man-Hei-Lee-Personal-planning-and-progress)
 - [Mark Richards](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki/Mark-Personal-Planning-and-Progress)
 - [Taeyoung Kim](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki/Taeyoung-Kim-Personal-Planning-and-Progress)
 - [Tongding Liu](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki/Tongding-Liu-Personal-Planning-and-Progress)
---

# Ethical Analysis
- [Ethical Analysis Wiki Page](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki/Ethical-Analysis)
---

# Group Processes (Issues + Wiki)
- [Team Contribution Wiki Page](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki)
- [Meeting Minutes Wiki Page](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki/Meeting-Minutes)
---

# Group Reflection
- [Group Reflection Wiki Page](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/wiki/Group-Reflection-on-Processes-and-Product)
---

# Product Notebook
Our complete analysis is documented in the product notebook, which performs all steps from data cleaning to final results presentation.

**Link to Product Notebook:** [Product Notebook](https://github.sydney.edu.au/fguo9672/2025-DATA3406-CC06-Group4/blob/main/Product_Notebook.ipynb)

The notebook includes:
- Initial assumptions and predictions
- Data cleaning and preprocessing
- Sleep/wake detection and classification
- Statistical analysis and hypothesis testing
- Comprehensive visualizations
- Final conclusions and limitations

---

# Product Notebook Results and Answering the Driving Question

## Overview

This report summarizes the key insights from our product notebook analysis and provides answers to the driving question: **Do they show variation in activity levels depending on their sleep/wake times or late-night activity?**

---

## Data Pipeline Summary

1. **Raw data:** Daily, hourly, and minute-level step counts
2. **Data cleaning:** Removed non-wear days (>75% zero hours) and corrected 
   sleep-period noise
3. **Descriptive analytics:** Inactivity pattern analysis, sleep/wake detection, 
   chronotype classification
4. **Statistical analysis:** t-tests for sleep timing, wake timing, and 
   late-night activity effects
5. **Final presentation:** Integrated visuals and narrative addressing the 
   driving question

---

## Adherence Analysis

### Methods
We computed adherence for each participant following Tang et al. (2018):
- **Adherence rate** = (valid days with StepTotal > 0) / (period days)
- **Hourly completeness** = (recorded hours) / (expected hours in period)
- **Gap analysis** = Count and length of data gaps

Participants were categorized as:
- High adherence (≥50%)
- Low adherence (<50%)

### Findings
- **Average adherence rate:** 84.4%
- **High adherence users:** 32 of 33 users (97.0%)
- **Users with gaps:** 15 of 33 (45.5%); gaps 1-7 days

### Impact on Results
- **Welch's t-test** between high/low adherence groups: Inconclusive 
  (insufficient samples in low adherence group; only 1 participant 
  had <50% adherence)
- **Pearson correlation** (adherence vs. daily variability): 
  r = 0.246, p = 0.167 (not significant)
- **Conclusion:** With 97% of participants showing high adherence (≥50%), 
  the dataset demonstrates generally excellent data quality. The lack of 
  significant correlation between adherence and activity variability, 
  combined with the high overall adherence rate, confirms that our main 
  findings are robust to data completeness differences and not artifacts 
  of measurement issues.

---

## Key Findings

### Sleep/Wake Pattern Detection
- **Sleep detected for:** 32 of 33 users (97.0%)
- **Average sleep duration:** 6.2 hours
- **Mean sleep start time:** 0.3 h (≈12:18 AM)
- **Mean wake time:** 6.5 h (≈6:30 AM)

**Sleep/Wake Pattern Distribution:**
- Early Sleeper / Early Riser: 18 users (56.2%)
- Early Sleeper / Late Riser: 7 users (21.9%)
- Late Sleeper / Late Riser: 7 users (21.9%)
- Late Sleeper / Early Riser: 0 users (0%)

### Statistical Tests: Sleep/Wake Timing Impact on Activity

#### 1. Sleep Time Impact
**t-test:** t = -0.477, p = 0.6365 → **NOT significant**
- High late-night group: 457.2 steps/hour (SD: 156.6)
- Low late-night group: 495.1 steps/hour (SD: 272.0)
- **Interpretation:** Sleep timing does not significantly predict overall 
  activity levels

#### 2. Wake Time Impact
**t-test:** t = -0.478, p = 0.6358 → **NOT significant**
- High late-night group: 451.6 steps/hour (SD: 178.0)
- Low late-night group: 483.3 steps/hour (SD: 194.9)
- **Interpretation:** Wake timing does not significantly predict overall 
  activity levels

#### 3. Late-Night Activity Impact
**t-test:** t = -1.298, p = 0.2041 → **NOT significant**
- High late-night activity group: 316.6 steps/hour (SD: 131.5)
- Low late-night activity group: 376.6 steps/hour (SD: 129.8)
- **Interpretation:** Late-night activity does not significantly predict 
  overall activity levels

**However, strong associations emerged:**
- 100% of Late Sleepers / Late Risers had high late-night activity
- 77.8% of Early Sleepers / Early Risers had low late-night activity
- Late-night activity reflects **timing redistribution** rather than volume changes

### Late-Night Activity Patterns
- **Mean late-night steps:** 70.6 steps/hour
- **Mean daytime steps:** 461.0 steps/hour
- **Median late-night/daytime ratio:** 0.10 (10% as active at night vs. day)

**Late-Night/Daytime Ratio by Sleep Pattern:**
- Early Sleeper / Early Riser: 0.097
- Early Sleeper / Late Riser: 0.162
- Late Sleeper / Late Riser: 0.357

### Data Quality Validation
- 97.0% of users had sufficient data for sleep detection
- Average 24.7 valid days per participant
- 87.3% daily data retention after cleaning
- Adherence analysis confirms findings are not artifacts of data quality issues

---

## Answer to the Driving Question

### **No** - No statistically significant variation detected

**Do participants show variation in activity levels depending on their 
sleep/wake times or late-night activity?**

While our analyses revealed strong **associations** between sleep/wake patterns 
and late-night activity (e.g., 100% of late sleepers had high late-night 
activity), **none** of the statistical tests showed significant differences in 
**overall activity levels**:

- Sleep timing: p = 0.6365 (not significant)
- Wake timing: p = 0.6358 (not significant)
- Late-night activity: p = 0.2041 (not significant)

### Key Interpretations

**1. Activity Timing vs. Activity Volume:**
The data shows that sleep/wake patterns affect **when** people are active 
(temporal distribution) rather than **how much** they move overall. 

**2. Strongest Association: Late-Night Activity**
Of the three factors examined, late-night activity showed the strongest 
association (p = 0.204, closest to significance):
- Lower late-night activity → slightly higher daytime activity (376.6 vs. 316.6 steps/hour)
- However, this 60-step difference was not statistically significant

**3. Circadian Pattern Alignment:**
- Late sleepers/risers show delayed activity peaks (later in the day)
- Early sleepers/risers show earlier activity peaks
- But total daily activity remains similar across groups

### Practical Implications

Despite the lack of statistical significance:
- **Sleep timing strongly predicts late-night behavior** (100% of late sleepers 
  had high late-night activity)
- **Activity redistribution occurs** across the day based on chronotype
- **Individual differences exist** but don't translate to overall activity variation

### Limitations

1. **Sample size:** N = 33 participants; may lack statistical power to detect 
   smaller effects
2. **Observation period:** 30 days; longer studies may reveal different patterns
3. **Sleep measurement:** Inferred from activity, not validated with sleep sensors
4. **Activity metric:** Step counts only; doesn't capture all movement types
5. **Statistical approach:** t-tests may not capture complex temporal patterns; 
   time-series or repeated measures ANOVA might reveal different insights

### Conclusion

While participants demonstrate clear patterns in **how** they distribute activity 
across the day (timing shifts based on sleep/wake schedules), these differences 
do not translate into statistically significant variation in **total** activity 
levels. The p-value of 0.204 for late-night activity suggests a trend toward 
association, but falls short of conventional significance thresholds.

**The study demonstrates that sleep/wake timing and late-night behavior influence 
activity distribution patterns, but not overall activity volume.** Future research 
with larger samples and more sophisticated temporal analyses may reveal whether 
these timing differences have health implications independent of total activity levels.

---
