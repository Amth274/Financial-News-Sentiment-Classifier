# Financial-News-Sentiment-Classifier


**Motivation**:
Market sentiment derived from news articles is one factor that can influence trading and investment decisions. By understanding the sentiment of financial news headlines, investors, traders, and financial institutions have another tool that they can use to make more informed decisions, assess risks, and potentially even design algorithmic trading strategies. This notebook demonstrates the process of training a RoBERTa model on the financial_phrasebank dataset that will be used to classify Marketwatch.com headlines into three sentiment categories: positive, neutral, and negative. While this exercise uses financial headlines as an input, the underlying techniques used in this notebook can be transferred to simmilar text classification tasks.
The methods outlined in this notebook also serve as a less-complicated, indirect sample for my actual data science work making a similar transformer model for multilabel text classification.

**Data Source**:
The financial_phrasebank dataset, labeled by annotators from the Aalto University School of Business, comprises sentiments of financial news headlines from companies listed in OMX Helsinki.

**Methodology**:
RoBERTa, a transformer model excelling in multiple NLP tasks, I chosen to leverage its advanced contextual understanding and exceptional text classification performance. The model processes unprocessed text to maintain semantic richness, leveraging attention mechanisms and optimized training to interpret nuanced language intricacies efficiently. Financial RoBERTa was used for the transfer learning opportunity, providing an enhanced understanding of financial texts, obtained from extensive fine-tuning on various financial documents (not including the financial phrasebank).

**Optimization**:
To combat extensive memory usage and computational slowdowns experienced in past projects, several optimizations were made. Mixed precision training and the 8BitAdam optimizer were employed to reduce memory footprint and accelerate training without significant performance loss. Early stopping was also implemented to prevent overfitting and unnecessary computations, essential for handling large datasets and intricate models efficiently.

**Results**:
The model demonstrated robust performance across various evaluation metrics. The following are the key results obtained post-evaluation:

'eval_loss': 0.2725694477558136<br>
'eval_accuracy': 0.9219653179190751<br>
'eval_precision_weighted': 0.9332768443366245<br>
'eval_precision_macro': 0.8964210324313951<br>
'eval_recall_weighted': 0.9219653179190751<br>
'eval_recall_macro': 0.940977432694182<br>
'eval_f1_weighted': 0.923649618171909<br>
'eval_f1_macro': 0.9146551438125865<br>
'eval_runtime': 3.9592<br>
'eval_samples_per_second': 87.391<br>
'eval_steps_per_second': 2.778<br>
'epoch': 15.0<br>

**Points of Consideration**:
While the model shows high reliability and accuracy in classifying financial news headlines, several considerations are crucial. The labeling process, involving multiple annotators, could introduce biases affecting the reliability of the dataset. Additionally, the specificity of the dataset to OMX Helsinki companies might limit the model's adaptability to diverse financial news sources and broader topics. Finally, the complex nature of transformer models like RoBERTa emphasizes the importance of interpretability in the financial sector to understand model predictions adequately for making informed decisions.
