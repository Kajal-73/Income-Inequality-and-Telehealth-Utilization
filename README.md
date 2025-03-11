Causal Inference

# Income Inequality and Telehealth Utilization: Exploring Socioeconomic Disparities in Access to Virtual Medical Appointments


## Introduction
This study examines the link between income and access to virtual medical appointments, a pressing issue amid telehealth's rapid growth during the COVID-19 pandemic. Telehealth expanded healthcare access while reducing in-person risks, but also exposed disparities, especially among underserved populations. Smith et al. found that telehealth adoption surged globally during the pandemic, providing essential healthcare access while mitigating risks of in-person contact.1 However, this rapid shift has also highlighted disparities in access, particularly for underserved populations.
Income and socioeconomic factors significantly influence telehealth accessibility. Uscher-Pines et al. found higher telehealth use among those with greater socioeconomic resources, while lower-income groups face barriers like unreliable internet and limited digital literacy, as highlighted by Roberts and Mehrotra.2, 3 Benda et al. identified broadband access as a key social determinant of health, with inequities in internet availability exacerbating disparities in telehealth adoption.4 These challenges underscore the dual potential of telehealth to reduce or widen healthcare inequities, stressing the need to address infrastructure gaps. Other factors also shape telehealth use. Employment stability facilitates access through health coverage and time flexibility, while women are more likely than men to utilize telehealth. Racial and ethnic disparities arise from systemic inequities like inadequate digital infrastructure. Insurance coverage remains a strong predictor of access, and transportation issues reflect broader socioeconomic inequalities that indirectly impact telehealth adoption.
Despite barriers, telehealth offers significant benefits for populations in rural and underserved areas by reducing transportation and geographic challenges.5 While telehealth can mitigate traditional barriers to care, its success depends on equitable access to technology and resources. Exploring these associations is critical for shaping policies to promote health equity. Data and Assumptions 
This study focuses on adults aged 18 and older, using data from the National Health Interview Survey (NHIS) for 2022 and 2023, to determine whether income levels significantly influence telehealth utilization.6 Specifically, this study seeks to answer the question: Does income from wages influence access to virtual medical appointments in the past 12 months? The study utilizes data from the NHIS 2022 and 2023, which surveyed adults aged 18 and older. Assumptions include the reliability of self-reported survey data and the adequacy of selected covariates—employment, gender, race/ethnicity, insurance coverage, and transportation availability—to address potential confounding. For data preprocessing, missing values were handled through imputation. Additionally, outliers were identified and addressed.

---
## Methods
Income and telehealth utilization were both recoded as binary variables, with other covariates, except race, also binary. Propensity score matching (PSM) was employed to control for confounding variables that could influence the relationship between income and telehealth access. Logistic regression was used to calculate propensity scores, and nearest neighbor matching was applied to ensure balanced covariates between the low-income (treated) and high-income (control) groups. After matching, telehealth utilization rates were analyzed through both outcome and sensitivity analyses. For the outcome analysis, post-matching differences in telehealth utilization were assessed using logistic regression for binary outcomes, ensuring that any imbalances in the outcome variable were appropriately addressed and did not bias the results. To strengthen the validity of the findings, a sensitivity analysis using Rosenbaum bounds was performed to assess the potential influence of unmeasured confounding on the treatment effect. To address substantial imbalances in the outcome variable across income groups while maintaining the representative nature of the data, a matched subset was analyzed to ensure greater comparability between the treatment and control groups.

---
## Results 
The balance of covariates improved significantly post-matching, as demonstrated by reduced standardized mean differences for all variables to below 0.1. The final matched dataset 
included 14,985 treated and 14,985 control individuals.
Matched analysis revealed that low-income individuals were significantly more likely to use telehealth services, with 35% of the low-income group reporting usage compared to 25% of the high-income group (χ² = 12.54, p < 0.001). Logistic regression supported our analysis by estimating telehealth usage (treated: 0.5774; control: 0.3859) as influenced by income from wages, adjusting for covariates like employment status (treated: 0.9524; control: 0.6434) and gender (treated: 0.5889; control: 0.4650), ensuring balanced comparison groups. Sensitivity analysis using Rosenbaum bounds indicated that results were significant to moderate levels of hidden biases, with γ values exceeding 1.5.
Looking at Figure 1 (Covariate Balance plot), we can observe that the matching process successfully improved balance across all key variables. The distance metric showed the largest initial difference (approximately 3.0 in the unadjusted sample), but was substantially reduced after matching. Employment status (EMPLASTWK_A) demonstrated the second-largest initial imbalance of around 1.0, which was also effectively reduced post-matching. Other covariates including sex (SEX_A), Hispanic/Latino ethnicity (HISPALLP_A), insurance coverage (NOTCOV_A), and transportation access (TRANSPOR_A) all showed minimal differences between groups after matching, with standardized mean differences falling within ±0.1.
Figure 2 (Outcome Distribution by Treatment Group) reveals the bimodal distribution of outcomes across both control and treated groups. The data shows two distinct peaks: one cluster around 0.0 with approximately 4,500 counts in each group, and another larger cluster around 1.0 with approximately 10,000 counts per group. This distribution pattern suggests that telehealth utilization tends to be polarized, with users either having very low or very high usage rates, and relatively few cases in between. The treated (low-income) and control (high-income) groups show similar patterns but with slightly different proportions  at each peak.
The Rosenbaum Sensitivity Analysis (Figure 3) demonstrates the robustness of our findings to unmeasured confounding. As gamma increases from 1.0 to 1.5, the upper bound p-value approaches but remains below 1.0, while the lower bound approaches 0. The analysis suggests that an unmeasured confounder would need to increase the odds of treatment assignment by a factor greater than 1.2 (where the upper bound crosses approximately 0.95) to potentially alter the study's conclusions. This indicates that our findings are effective to hidden bias, as such a large effect from an unmeasured confounder is unlikely given the comprehensive set of covariates already included in the analysis.

---
## Discussion
This study identifies a significant relationship between income and telehealth utilization, with low-income individuals showing higher adoption rates. This suggests that telehealth may help address traditional healthcare access barriers like transportation and geographic isolation. However, increased adoption does not imply optimal utilization, as factors such as limited internet access, digital literacy, and health infrastructure may still impede effective use. Insurance coverage and provider outreach also influence telehealth adoption, with insured individuals having better access to services.
The study's limitations include reliance on self-reported data and the cross-sectional design, which prevents establishing causal relationships. Future research should explore the long-term effects of income on telehealth adoption through longitudinal studies and examine additional factors like digital literacy and internet access. Further investigation into the role of healthcare providers in facilitating access for underserved populations is essential to ensure equitable telehealth access across socioeconomic groups.

---
## Conclusion 
This study provides compelling evidence that income plays a significant role in shaping telehealth access, with low-income individuals being more likely to utilize telehealth services compared to higher-income individuals. These findings highlight the potential of telehealth to reduce traditional healthcare access barriers, such as transportation and geographic isolation, and improve healthcare delivery for underserved populations. However, the study also emphasizes that the benefits of telehealth adoption may not be fully realized unless structural and infrastructural barriers, such as internet access, digital literacy, and insurance coverage, are addressed.
The results of this study contribute to the broader discourse on healthcare equity in a digital age, emphasizing the need for targeted interventions and policies that ensure digital health equity. By focusing on income and other socioeconomic factors, this research informs ongoing efforts to make telehealth a tool for improving health outcomes across all populations, ensuring that no one is left behind in the digital transition of healthcare services. Moving forward, continued research will be crucial to better understand the full scope of factors that influence telehealth adoption and to develop strategies that promote equitable access for all.

---
## References
Smith AC, Thomas E, Snoswell CL, et al. Telehealth for global emergencies: Implications for coronavirus disease 2019 (COVID-19). J Telemed Telecare. 2022;28(1):3-11. doi:10.1177/1357633X20916567
Uscher-Pines L, Sousa J, Jones M, et al. Telehealth use for primary and specialty care during the COVID-19 pandemic among fee-for-service Medicare beneficiaries. JAMA Netw Open. 2020;3(9):e2033962. doi:10.1001/jamanetworkopen.2020.33962
Roberts ET, Mehrotra A. Assessment of disparities in digital access among Medicare beneficiaries and implications for telemedicine. JAMA Intern Med. 2020;180(10):1386-1389. doi:10.1001/jamainternmed.2020.2666
Benda NC, Veinot TC, Sieck CJ, et al. Broadband internet access is a social determinant of health. Am J Public Health. 2022;112(4):614-620. doi:10.2105/AJPH.2021.306649
Totten AM, Womack DM, Eden KB, et al. Telehealth: Mapping the evidence for patient outcomes from systematic reviews. Agency for Health Res and Quality. 2016. 
National Center for Health Statistics. National Health Interview Survey (NHIS): Survey documentation. CDC. Updated 2024. 
