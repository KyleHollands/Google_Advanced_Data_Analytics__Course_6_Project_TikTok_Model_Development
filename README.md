# Google_Advanced_Data_Analytics__Course_6_Project_TikTok_Model_Development

The goal of this project was to develop a model that could accurately classify TikTok videos as containing either a claim or an opinion based on their content.

Both Random Forest and XGBoost models were built, evaluated, and tested on a validation set to select a champion model, which was then tested on a holdout set to assess its performance on unseen data.

Additionally, tokenization of video transcription text was performed to identify any keywords in TikTok videos that indicated a claim or opinion. The top 15 tokenized phrases, with a range of 2-3 ngrams, were used as features in the model. However, it was later determined that these phrases had low predictive power compared to video engagement metrics.

Both the Random Forest and XGBoost models performed exceptionally well, with high Precision, Recall, and F1 scores. Recall was particularly important due to the higher impact of type 2 errors, where a claim is falsely classified as an opinion.

The importance of a model like this cannot be understated due to the significant negative impact misinformation can have on online platforms like TikTok, which are seen, believed, and shared by millions of people.