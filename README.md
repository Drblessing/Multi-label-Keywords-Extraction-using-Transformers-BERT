# Multi Label Keywords Extraction using Transformers (BERT)

Text Classification using Transformers (BERT) for predicting multi-label tags for questions posted on Stack Exchange. Data can be found on Kaggle: https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/data 

--------------------------------- 

The dataset is 7.25GB and contains 4 columns: Id, Title, Body & Tags:
- Id - Unique identifier for each question
- Title - The question's title
- Body - The body of the question
- Tags - The tags associated with the question

Question Body and Title have varying lengths, and the number of Tags associated with each question varies. There are in total approx—27,000 unique Tags.

My approach to this task was to use a pre-trained model from Hugging Face, specifically the BERT base cased model with the MultiLabelBinarizer from scikit-learn to encode the target.

The notebook is constructed to train and process the whole 7.25 GB dataset in Google CoLab Pro without breaking the kernel (but due to time restrictions not trained on the full dataset).

To further restrict the complexity of this task, I focused on only classifying the top 10 Tags in the dataset (please see notebook for more information).

The final performance of the model yields a accuracy of 93%. 

Further improvements to this model include:
- Experiment more with increasing the number of tags our model can classify
- Reducing required training time of model
- Compare performance with other pre-trained BERT models
- Try other keywords/topic extraction, specific models

References: https://medium.com/analytics-vidhya/multi-label-text-classification-using-transformers-bert-93460838e62b
