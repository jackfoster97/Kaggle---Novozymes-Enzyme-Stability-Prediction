# Kaggle---Novozymes-Enzyme-Stability-Prediction

This attempt at the Kaggle competition for predicting enzyme stability: https://www.kaggle.com/competitions/novozymes-enzyme-stability-prediction/data 

Information about the dataset: 

train.csv - the training data, with columns as follows:

    seq_id: unique identifier of each protein variants
    
    protein_sequence: amino acid sequence of each protein variant. The stability (as measured by tm) of protein is determined by its protein sequence. (Please note that most of the sequences in the test data have the same length of 221 amino acids, but some of them have 220 because of amino acid deletion.)
    
    pH: the scale used to specify the acidity of an aqueous solution under which the stability of protein was measured. Stability of the same protein can change at different pH levels.
    
    data_source: source where the data was published
    
    tm: target column. Since only the spearman correlation will be used for the evaluation, the correct prediction of the relative order is more important than the absolute tm values. (Higher tm means the protein variant is more stable.)

train_updates_20220929.csv - corrected rows in train, please see this forum post for details

test.csv - the test data; your task is to predict the target tm for each protein_sequence (indicated by a unique seq_id)

sample_submission.csv - a sample submission file in the correct format, with seq_id values corresponding to test.csv

wildtype_structure_prediction_af2.pdb - the 3 dimensional structure of the enzyme listed above, as predicted by AlphaFold