# R-BERT and R-RoBERTa model on custom dataset

## Dataset Details :-
	Train set - 16784
	Test set - 175 (5 examples per label)
	no of labels - 35

## Accuracy
	R-BERT - 91.43% (after 2 epoch of training ~ 25 mins on Tesla K80 colab free GPU)
	R-RoBERTa - 86.29% (after 3 epochs of training ~ 25 mins on Tesla T4 colab free GPU)

## Hyperparameters
	Max sequence length was kept as 128 for both the models
	{Data examples having entity 1 or entity 2 present after 128 length in sequence were not used in training} 

## Drive link for trained models and logs
	https://drive.google.com/drive/folders/1GYEGvW9VhQpMc9c0FcpyBpzsLdtsXxmg?usp=sharing