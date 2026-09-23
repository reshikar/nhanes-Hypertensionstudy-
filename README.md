NHANES Hypertension Analysis Report
1. Objective

The objective of this analysis was to estimate the prevalence of hypertension among U.S. adults using NHANES 2021–2023 data and examine demographic and cardiometabolic factors associated with hypertension while accounting for the complex NHANES survey design.

2. Data Source and Study Population

Data were obtained from the 2021–2023 National Health and Nutrition Examination Survey (NHANES). Demographic, body measurement, blood pressure examination, blood pressure questionnaire, diabetes, physical activity, and smoking datasets were linked using the unique participant identifier (SEQN).

The analysis was restricted to adults aged 20 years or older. The initial adult analytic sample included 7,809 participants.

3. Outcome Definition

Hypertension was defined using measured blood pressure and antihypertensive medication use. Participants were classified as having hypertension when they met at least one of the following criteria:

mean systolic blood pressure ≥130 mmHg;
mean diastolic blood pressure ≥80 mmHg; or
current use of antihypertensive medication.

Mean systolic and diastolic blood pressures were calculated from available oscillometric measurements.

Note for final report: We still need to verify the BP averaging procedure and hypertension definition against the official 2021–2023 NHANES documentation before treating this section as final.

4. Covariates

The analysis considered age group (20–39, 40–59, and ≥60 years), sex, race/ethnicity, educational attainment, BMI category, diabetes status, and cigarette-smoking status.

BMI was categorized as underweight, normal weight, overweight, or obesity. Diabetes was based on self-reported physician-diagnosed diabetes, and smoking status was categorized as never, former, or current smoking.

5. Statistical Analysis

NHANES examination weights (WTMEC2YR), masked variance strata (SDMVSTRA), and primary sampling units (SDMVPSU) were incorporated using the R survey package.

Survey-weighted hypertension prevalence and 95% confidence intervals were estimated overall and across demographic and clinical subgroups.

An initial multivariable model containing age, sex, race/ethnicity, BMI, diabetes, education, and smoking exceeded the available survey design degrees of freedom and did not provide valid p-values. The primary adjusted model was therefore specified more parsimoniously using age group, sex, BMI category, and diabetes status.

Because hypertension was common in the study population, survey-weighted Poisson regression with a log link was subsequently used to estimate adjusted prevalence ratios (aPRs) and 95% confidence intervals.

6. Results

Hypertension prevalence increased substantially with age. Weighted prevalence was 24.9% (95% CI: 22.0%–27.9%) among adults aged 20–39, 52.8% (95% CI: 50.2%–55.3%) among those aged 40–59, and 72.0% (95% CI: 69.6%–74.5%) among adults aged ≥60 years. Prevalence was 45.9% among females and 52.7% among males.

There were also descriptive differences across race/ethnicity. Hypertension prevalence was 50.1% among non-Hispanic White adults, 60.9% among non-Hispanic Black adults, 40.5% among Mexican American adults, 41.3% among other Hispanic adults, 41.8% among non-Hispanic Asian adults, and 49.4% among adults classified as other/multiracial. These estimates are unadjusted and should not be interpreted as independent effects of race/ethnicity.

A gradient was observed across BMI categories. Weighted hypertension prevalence was 33.5% among adults with normal weight, 44.6% among adults with overweight, and 63.7% among adults with obesity. The estimate among underweight adults was 16.1%, although this group was comparatively small.

Hypertension prevalence was 76.5% among adults with diabetes, compared with 45.5% among adults without diabetes. Prevalence was 44.6% among never smokers, 59.8% among former smokers, and 51.7% among current smokers.

Adjusted analysis

After simultaneous adjustment for age group, sex, BMI category, and diabetes status, several factors remained associated with hypertension.

Compared with adults aged 20–39 years, hypertension prevalence was 1.96 times higher among adults aged 40–59 years (aPR 1.96; 95% CI: 1.76–2.18) and 2.74 times higher among adults aged ≥60 years (aPR 2.74; 95% CI: 2.40–3.12).

Male adults had 1.17 times the prevalence of hypertension compared with female adults (aPR 1.17; 95% CI: 1.11–1.23).

Compared with adults with normal BMI, hypertension prevalence was 22% higher among adults with overweight (aPR 1.22; 95% CI: 1.08–1.39) and 74% higher among adults with obesity (aPR 1.74; 95% CI: 1.57–1.94). The underweight group had a lower estimated prevalence (aPR 0.52; 95% CI: 0.34–0.81).

Adults with diabetes had approximately 17% higher adjusted prevalence of hypertension than adults without diabetes (aPR 1.17; 95% CI: 1.12–1.23).

7. Interpretation

The analysis demonstrates substantial variation in hypertension prevalence across demographic and cardiometabolic characteristics. Age showed the strongest adjusted association, with hypertension prevalence increasing markedly among middle-aged and older adults. Higher BMI was also associated with progressively greater hypertension prevalence, particularly among adults with obesity.
Diabetes and male sex were independently associated with higher hypertension prevalence after adjustment for age and BMI.

Table 1. Survey-weighted prevalence of hypertension among U.S. adults, NHANES 2021–2023
| Characteristic      | Weighted prevalence (%) | 95% CI (%) |
| ------------------- | ----------------------: | ---------: |
| **Sex**             |                         |            |
| Female              |                    45.9 |  43.4–48.4 |
| Male                |                    52.7 |  50.2–55.1 |
| **Age group**       |                         |            |
| 20–39 years         |                    24.9 |  22.0–27.9 |
| 40–59 years         |                    52.8 |  50.2–55.3 |
| ≥60 years           |                    72.0 |  69.6–74.5 |
| **Race/ethnicity**  |                         |            |
| Non-Hispanic White  |                    50.1 |  47.6–52.5 |
| Non-Hispanic Black  |                    60.9 |  56.1–65.7 |
| Mexican American    |                    40.5 |  32.7–48.3 |
| Other Hispanic      |                    41.3 |  33.9–48.6 |
| Non-Hispanic Asian  |                    41.8 |  35.4–48.2 |
| Other/Multiracial   |                    49.4 |  43.1–55.6 |
| **BMI category**    |                         |            |
| Normal weight       |                    33.5 |  30.8–36.2 |
| Underweight         |                    16.1 |   9.8–22.3 |
| Overweight          |                    44.6 |  40.8–48.3 |
| Obesity             |                    63.7 |  60.3–67.2 |
| **Diabetes status** |                         |            |
| No                  |                    45.5 |  43.5–47.6 |
| Yes                 |                    76.5 |  74.1–78.9 |
| **Smoking status**  |                         |            |
| Never               |                    44.6 |  42.0–47.3 |
| Former              |                    59.8 |  57.0–62.6 |
| Current             |                    51.7 |  46.9–56.6 |




Table 2. Adjusted prevalence ratios for hypertension
| Characteristic      |       aPR |    95% CI |
| ------------------- | --------: | --------: |
| **Age group**       |           |           |
| 20–39 years         | Reference |         — |
| 40–59 years         |  **1.96** | 1.76–2.18 |
| ≥60 years           |  **2.74** | 2.40–3.12 |
| **Sex**             |           |           |
| Female              | Reference |         — |
| Male                |  **1.17** | 1.11–1.23 |
| **BMI category**    |           |           |
| Normal weight       | Reference |         — |
| Underweight         |  **0.52** | 0.34–0.81 |
| Overweight          |  **1.22** | 1.08–1.39 |
| Obesity             |  **1.74** | 1.57–1.94 |
| **Diabetes status** |           |           |
| No                  | Reference |         — |
| Yes                 |  **1.17** | 1.12–1.23 |

Note. aPR = adjusted prevalence ratio; CI = confidence interval. Estimates are from survey-weighted Poisson regression with a log link and are mutually adjusted for age group, sex, BMI category, and diabetes status.
Table 3. Adjusted odds ratios for hypertension — secondary analysis
| Characteristic      |       aOR |    95% CI |
| ------------------- | --------: | --------: |
| **Age group**       |           |           |
| 20–39 years         | Reference |         — |
| 40–59 years         |      3.06 | 2.67–3.50 |
| ≥60 years           |      7.98 | 6.39–9.95 |
| **Sex**             |           |           |
| Female              | Reference |         — |
| Male                |      1.48 | 1.29–1.68 |
| **BMI category**    |           |           |
| Normal weight       | Reference |         — |
| Underweight         |      0.40 | 0.23–0.71 |
| Overweight          |      1.42 | 1.10–1.82 |
| Obesity             |      3.56 | 2.81–4.51 |
| **Diabetes status** |           |           |
| No                  | Reference |         — |
| Yes                 |      1.84 | 1.53–2.21 |


Note. aOR = adjusted odds ratio. Estimates are from the reduced survey-weighted logistic regression model and are mutually adjusted for age group, sex, BMI category, and diabetes status.



Because these data are cross-sectional, the associations should not be interpreted as causal relationships.
