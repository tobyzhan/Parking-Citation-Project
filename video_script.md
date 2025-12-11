# Video Script: San Diego Parking Citations Clustering Analysis
## 5-Minute High-Level Overview

**Duration: ~5 minutes**  
**Team: Toby Zhang, Rohan Marda, Luke Huang, Tyler Wong**

---

## [0:00-0:30] INTRODUCTION & HOOK (30 seconds)

**[Visual: San Diego street map with citation hotspots lighting up]**

**Speaker:**
"Have you ever wondered why some San Diego streets seem to have parking enforcement everywhere, while others barely see a ticket? In 2024, San Diego issued nearly half a million parking citations, generating over $26 million in revenue. But here's the interesting part: this enforcement isn't spread evenly across the city. A handful of streets like 4th Avenue, Mission Boulevard, and Island Avenue account for a massive portion of all tickets written.

Today, we're going to show you how we used data science to uncover hidden patterns in San Diego's parking enforcement landscape."

---

## [0:30-1:15] RESEARCH QUESTION & MOTIVATION (45 seconds)

**[Visual: Research question text on screen]**

**Speaker:**
"Our research question was: Can San Diego streets be grouped into distinct, meaningful clusters based on their citation patterns? And if so, do these clusters show significant differences in the types of violations and fine amounts?

This matters because parking citations aren't just about following rules—they impact city revenue, neighborhood equity, and how communities experience enforcement. Previous research has shown that citation burdens often fall unevenly across different communities, so understanding these patterns is crucial for fair policy-making."

---

## [1:15-2:15] DATA & METHODOLOGY (60 seconds)

**[Visual: Dataset stats and data cleaning flowchart]**

**Speaker:**
"We analyzed 475,638 parking citations from San Diego's 2024 public dataset. This included information about where citations were issued, what violations occurred, and how much each fine cost.

First, we cleaned the data by standardizing street names and removing rare violation types. Then, we aggregated citations by street location to create our analysis units.

**[Visual: Feature engineering diagram]**

Our approach involved two clustering models. The baseline model used just total citations and average fines per street. But we didn't stop there. We engineered richer features including:
- Day-of-week patterns
- Seasonal distributions  
- Violation type proportions

This gave us a much more complete picture of enforcement patterns beyond just raw numbers."

---

## [2:15-3:15] KEY FINDINGS - CLUSTERING RESULTS (60 seconds)

**[Visual: Cluster visualization with PCA plot]**

**Speaker:**
"Here's what we discovered. When we used K-means clustering, the data naturally split into two distinct groups.

**[Visual: Cluster 0 characteristics]**

Cluster 0: The 'Typical Streets' - This is the majority of San Diego streets. They have moderate citation volumes with a mix of violation types—things like street sweeping, violation of posted signs, and registration issues. These streets see routine, low-intensity enforcement.

**[Visual: Cluster 1 characteristics]**

Cluster 1: The 'Enforcement Hotspots' - A much smaller group of streets concentrated in downtown and commercial areas. These locations have extremely high citation volumes and are dominated by specific violations like expired meters, passenger loading zones, and time-limited parking. These are your high-turnover commercial corridors where enforcement is constant.

**[Visual: Silhouette score comparison]**

The engineered features model achieved a silhouette score of 0.45, significantly better than our baseline. This tells us the two-cluster solution captures real, meaningful differences in enforcement patterns."

---

## [3:15-4:15] KEY FINDINGS - STATISTICAL VALIDATION (60 seconds)

**[Visual: Statistical test results dashboard]**

**Speaker:**
"But we didn't just stop at clustering—we validated these differences with rigorous statistical tests.

**[Visual: Chi-square test results]**

First, a chi-square test confirmed that violation types are NOT independent of cluster membership. In other words, different clusters really do have different violation profiles. This was statistically significant with a p-value far below 0.05.

**[Visual: ANOVA/Kruskal-Wallis results]**

Second, we tested whether fine amounts differ across clusters. While the Kruskal-Wallis test showed significant differences in fine distributions, the effect wasn't as dramatic as the violation type differences. Typical streets actually had slightly higher average fines due to occasional high-penalty violations, while hotspots had more consistent, moderate fines from meter and loading violations.

**[Visual: Proportion test results]**

Finally, proportion tests revealed which specific violations drive cluster differences. Hotspot streets have significantly higher proportions of expired meter and passenger loading violations, while typical streets see more street sweeping and sign violations."

---

## [4:15-4:50] LIMITATIONS & ETHICAL CONSIDERATIONS (35 seconds)

**[Visual: Ethics checklist highlights]**

**Speaker:**
"Now, let's be honest about limitations. We only analyzed one year of data, so we can't say if these patterns hold over time. We also only see where enforcement happens—not where violations actually occur. This is crucial because enforcement decisions could introduce bias.

We carefully considered the ethical implications. Our analysis doesn't identify specific neighborhoods or demographics, but previous research suggests enforcement can disproportionately impact certain communities. That's why we emphasize: this is descriptive research, not a prescription for where police should patrol."

---

## [4:50-5:00] CONCLUSION & IMPACT (10 seconds)

**[Visual: Key takeaway text]**

**Speaker:**
"The bottom line? San Diego's parking enforcement isn't random—it's highly concentrated. A small number of hotspot streets drive most of the city's citation activity, while the majority of streets experience routine, low-intensity enforcement. Understanding these patterns is the first step toward more equitable and data-informed parking policy.

Thank you for watching!"

---

## VISUAL SUGGESTIONS FOR EACH SECTION

1. **Introduction**: Animated map showing citation density across San Diego
2. **Research Question**: Clean text slides with key question highlighted
3. **Data & Methodology**: Flowchart showing data pipeline, feature engineering diagram
4. **Clustering Results**: PCA scatter plot, cluster characteristic comparison table
5. **Statistical Validation**: Test result tables with p-values highlighted, bar charts comparing proportions
6. **Limitations**: Quick bullet points, ethics checklist
7. **Conclusion**: Summary infographic with main finding

---

## TIMING BREAKDOWN
- Introduction: 30 seconds
- Research Question: 45 seconds  
- Data & Methodology: 60 seconds
- Clustering Findings: 60 seconds
- Statistical Validation: 60 seconds
- Limitations & Ethics: 35 seconds
- Conclusion: 10 seconds

**Total: 5 minutes**

---

## SPEAKER NOTES

- **Pace**: Conversational but clear, ~140-150 words per minute
- **Tone**: Professional yet accessible—explain technical concepts without jargon
- **Emphasis**: Stress the practical implications and real-world relevance
- **Transitions**: Use visual cues to guide viewers through each section
- **Call-out**: When showing statistical tests, briefly explain what the p-values mean in plain language
