# acppred

By Alessandra Neis

ACPPred is a machine-learning tool designed for anticancer peptide prediction. We trained this model based on anticancer peptide libraries experimentally tested through the Random Forest algorihtm. For software development, we used a series of objects to define each activity to be performed through functions of the calss Model, in which the maisn are 'transform', 'train', and 'predict'. In 'transform', we estimated the amino acid percentage for positive and negative peptides, which enables us to predict the probability of another peptide to present antitumoral activity using ProtParam.ProteinAnalysis package. In 'train', the sci-kit learn package was used to train a model with the aforementioned subset of sequences, divided in train and test. In 'predict', it is possible to input a sequence and analyze its probability of being an antitumoral peptide, in which we obtained an f1-score of 0.92 and 0.91 for negative and positive peptides, respectively. We extensively tested all our objects in the code through PyTest.

The only requirement to use both the webserver or standalone version of ACPPred is a fasta formatted sequence as input. The output is a .csv table containing the probability for the given peptide to present antitumoral activity (0-100%). The option --model also required a file and the trained model path is ~/acppred/data/models/model.pickle.

## Setup

```
$ make setup
```
