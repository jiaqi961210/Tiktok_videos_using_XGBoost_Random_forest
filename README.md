# Tiktok_videos_using_XGBoost_Random_forest

## Introduction

TikTok allows users to report videos that may violate its terms of service, leading to a high volume of reports, far too many for human moderators to handle individually. Our analysis indicates that videos violating terms are more likely to contain claims rather than opinions, making it crucial to distinguish between the two.

TikTok plans to develop a machine learning model to classify videos as either claims or opinions. Videos identified as opinions will have a lower priority for human review, while claim videos will be further processed to determine their review priority, possibly ranked by the number of reports they receive.

### 1.Targeting variable for the model

The model's target variable will be "claim_status," a binary indicator of whether a video is a claim or an opinion. This classification task will help moderators focus on the videos most likely to violate TikTok's terms of service.

### 2. Evaluation metric

In this scenario, it's more critical for the model to err on the side of false positives rather than false negatives. Identifying videos that violate the terms of service is paramount, even if some opinion videos are mistakenly flagged as claims. If an opinion is misclassified as a claim, the worst outcome is that it undergoes human review. However, if a claim is incorrectly classified as an opinion, it might not be reviewed at all, potentially allowing a violation to go unnoticed. Since minimizing false negatives is crucial, the model evaluation metric will focus on recall.
