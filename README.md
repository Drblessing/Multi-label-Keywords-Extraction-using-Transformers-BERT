# Multi Label Keywords Extraction using Transformers (BERT)

Text Classification using Transformers (BERT) for predicting multi-label tags for questions posted on Stack Exchange. Data can be found on Kaggle: https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/data 

--------------------------------- 

The dataset is 7.25GB and contains 4 columns: Id, Title, Body & Tags:
- Id - Unique identifier for each question
- Title - The question's title
- Body - The body of the question 
- Tags - The tags associated with the question

Question Body and Title both has varying length, and the number of Tags associated to each question varries. 
There is in total approx. 27,000 unique Tags. 

My approach to this task was to use the a pretrained model from Hugging Face, specifially the BERT base cased model with the MultiLabelBinarizer from scikit-learn to encode the target. 

The notebook is constructed to train and process the whole 7.25 GB dataset in Google CoLab Pro without breaking the kernel (but due to time restriction not trained on the full dataset). 

To further restrict the complexity of this task, I focused on only classifying the top 100 Tags in the dataset (please see notebook for more information).

The final performance of the model yield a F1 score of ... 

Futher improvements to this model includes: 
- Experiment more with increasing the number of tags our model can classify
- Reducing required traning time of model 
- Compare performance with other pre-trained BERT models
- Try other keyword/topic extraction specific models

