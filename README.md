## Data-Bias

The goal of this project is to explore whether or not bias might affect the results of the Perspective API tool, which is a free API that uses machine learning to identify and give a score to "toxic" comments. To achieve this we are using a dataset of Wikipedia comments that contais a series of binary labels applied by human raters: "toxic," "severe_toxic," "obscene," "threat," "insult," and "identity_hate."

The first step I took in this process was exploring and cleaning the unlabeled data, because I noticed that there were some toxic comments, or at least, comments that contains insults that were accurately scored by the API tool, but didn't received any label.

Next I created an string column with the combination of labels per row and used this to create a dataframe with information of each unique category. Information such as the mean score per category and the count and rates of unique comments that received a higher score than certain threshold in an arange of values from 0 to 1 with steps of 0.5.

That process allowed me to show that there was some bias in the API tool related with the category of 'identity hate' and inaccurate scores given by some 'special' vocabulary.


