# Fake-News-Classifier-Using-LSTM

In this Project, We need to classify the whether the News is fake or genuine by using NLP techniques.
Here, We'll take the sentences and apply one hot representation on top of it and then pass it to the embedding layer and then pass it to the LSTM and train that particular model.

So, First thing First, After analysing the data, I've tried Cleaning the data by removing some missing values
and then assigned the label column to the Y variable as it was dependent variable and rest of the features in X variable.

I've imported 
-Embedding Layers
-Pad sequences (when we pass the input to embedding layer, we need to ensure the input size fixed), so we can add pad either on pre side or post side so that sentences will be equal in length. 
-Sequential ( for Creating Sequential Model)
-one_hot (for converting sentences into one hot representation given a vocabulary size)
-LSTM (for LSTM layer)
-Dense ( for Dense Layer)
-Nltk (for stopwords, porterstemmer,etc)

Then assigned a value to vocabulary size within which we will get the sentences. 

Then After removing stop words, I've preprocessed the data using Stemming technique and with regular expressions I've substituted everything with a blank apart from words which are in A-Z and iterating through the titles(news headlines)

After this, I am also lowering down the words of the sentences and splitting the data.
I've stored this preprocessed data in the corpus. 

Then, I've converted the words to one hot representation, so all the words got converted into that specific index

After that, I've used pad sequences for pre padding for fixed input size

Then, I've Created a model where I've defined the vector features, then created a Sequential layer, Embedding layer.

I'm passing the output generated from the Embedding layer to the LSTM layer. where I've taken 1 LSTM layer which is having 100 neurons.
then added the Dense layer since it is a classification problem where I've used sigmoid Activation function.
then Compiled the model with the Adam optimizer, binary cross entropy loss function.

After that, splitted into train/test with test size as 0.33 . Then fitted the model passing epoch and batch size value. 
For further hyper parameter tuning, I've tried adding drop out layer after embedding layer and LSTM layer.
