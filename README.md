# Tree-Based Classification Model for Predicting Video Claims or Opinions

## Project Overview
The goal of this analysis was to analyze TikTok video data and develop a model capable of predicting whether the content within these videos contains claims or opinions. The final model created was a Random Forest model, which achieved an impressive accuracy score of 99.76%, a recall of 99.53%, and an F1 score of 99.77%. The model identified the most influential features that determine whether a video contains a claim or an opinion. The key factors included 'video_view_count,' 'video_like_count,' 'video_share_count,' 'video_download_count,' and 'video_comment_count.'

## Business Understanding
The primary stakeholders for this project are the TikTok department responsible for auditing user submissions regarding whether a video contains a claim. Developing a predictive model will significantly accelerate the process of identifying these videos, enabling quicker actions to reduce harmful and misleading content from being seen by a large audience.

## Data Understanding
The dataset utilized in this analysis consists of 19382 rows and 12 features related to video information, encompassing various data types (int64, float64, and object). To prepare the data for further analysis and modeling, I addressed missing values, duplicates, and outliers. I also examined the imbalance in the outcome variable 'claim_status' to determine whether class balancing was necessary; ultimately, it was not required. An additional feature, 'text_length,' was derived from the existing 'video_transcription_text' variable and was subsequently visualized and incorporated into the model.

## Modeling and Evaluation
Before model development, tokenization of the video transcription text was carried out to identify keywords that indicated claims or opinions in TikTok videos. The top 15 tokenized phrases, covering 2-3 n-grams, were initially included as features in the model. However, it was later concluded that these phrases possessed low predictive power compared to video engagement metrics. The final Random Forest model was used to pinpoint the most predictive features for determining whether a video contained a claim or an opinion. The evaluation scores demonstrate robust performance, particularly in terms of recall, which is vital for minimizing false negatives. In this context, false negatives could result in harmful content being misclassified as opinions, which could lead to significant harm.

### Feature Importances
- video_view_count: 0.579029
- video_like_count: 0.276727
- video_share_count: 0.066875
- video_download_count: 0.041710
- video_comment_count: 0.020514

### Model Scoring Metrics
- Accuracy: 0.9976
- Precision: 1.000
- Recall: 0.9953
- F-score: 0.9977

## Conclusion
The analysis concluded that video engagement metrics, such as 'video_view_count,' 'video_like_count,' 'video_share_count,' 'video_download_count,' and 'video_comment_count,' serve as strong indicators that a video contains a claim and has gone viral. Given the model's strong predictive capabilities, it is recommended to begin testing it on additional subsets of real user data to assess performance, with the potential for future production use. The significance of a model like this cannot be overstated due to the considerable negative impact misinformation can have on online platforms like TikTok, which are viewed, believed, and shared by millions of users.
