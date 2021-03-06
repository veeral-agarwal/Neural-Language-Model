# Neural Language Model 

done as an assignment of Introduction of Natural Language Processing course, NLP | Spring 2021

## how to run : 
upload datasets on drive and run the notebook on google colab. 

## Average Perplexities

Kneser Training: 3.5826378214803802 <br>
Kneser Testing: 532.1675432788799 <br>
Kneser Validation: 454.13629989185324 <br>

Witten Training: 2.710249953959174 <br>
Witten Testing: 21873464.425774388 <br>
Witten Validation: 20906925.301411595 <br>

LSTM Training = 14879.11386069286 <br>
LSTM Testing  = 39688.13258867951 <br>
LSTM Validation = 21781.48651231239 <br>

## Analysis

The first thing to mention is that the perplexity calculated in LSTM is much different from the one in the other two statistical methods. This is probably because of a difference in how it's calculated. https://stackoverflow.com/questions/59209086/calculate-perplexity-in-pytorch was used as a reference. Also an important thing to note is how similar training is to Testing and validation. The reason for this is also unclear, and some parameter tuning was done. It is possible the model is underfitting, however it starts to overfit on other cases. A possible way to resolve this is by doing a grid search.

Note that only a subset was taken for the Statistical LM due to the running time. 

For the Statistical LMs, we get a large difference between testing and training/validation. This is understandable, due to how OOV words are dealt with, vastly increasing the perplexity.
