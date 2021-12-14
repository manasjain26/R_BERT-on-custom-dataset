# R-BERT and R-RoBERTa model on custom dataset

## Dataset Details :-
	Train set - 16784
	Test set - 175 (5 examples per label)
	no of labels - 35
	(You can find the data files in the data folder inside R-BERT and R-RoBERTa folders)
## Accuracy
	R-BERT - 91.43% (after 2 epoch of training ~ 25 mins on Tesla K80 colab free GPU)
	R-RoBERTa - 86.29% (after 3 epochs of training ~ 25 mins on Tesla T4 colab free GPU)

## Hyperparameters
	Max sequence length was kept as 128 for both the models
	{Data examples having entity 1 or entity 2 present after 128 length in sequence were not used in training} 

## Drive link for trained models and logs
	https://drive.google.com/drive/folders/1GYEGvW9VhQpMc9c0FcpyBpzsLdtsXxmg?usp=sharing
	
# Fine-tuning of MuRIL on the above dataset (Findings)

## Accuracy
	Fine-tune MuRIL - after 3 epochs, training accuracy was around 16% and test set accuracy was just 2%. (used TensorFlow framework)
	
# Future work and important ideas discussed 
1) different formats of training data. i) replacing entities with their entity label ii) NER labels will be added with the entity.
2) concept of bag of sentences which will be useful in denoising the dataset
3) SpERT model Github (Points I feel are important for this task link - https://github.com/lavis-nlp/spert Reference issue link - https://github.com/lavis-nlp/spert/issues/30 (last 2 comments)). Hence Even if we train the SpERT model on our data at the time of inference we won't be able to provide e1 and e2 entity pair, relation we want to predict.
