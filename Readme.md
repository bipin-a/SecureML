# File Structure

Notebooks are used to generate attacks on a victim model. 

The following are models which have been attacked:
"textattack/bert-base-uncased-imdb",
"textattack/distilbert-base-uncased-imdb",
"textattack/albert-base-v2-imdb",
"adv_trained_model/best_model"  

##adv_trained_model/best_model## is a local model, produced by running "adv_training_bert.ipynb" notebook.


The following are perturbed datasets produced by the respective attack and have a corresponding notebook which produced the dataset: 
"log_A2TYoo2021_0.05",
"log_A2TYoo2021_0.1",
"log_A2TYoo2021_0.15",
"log_TextFoolerJin2019",
"log_BAEGarg2019",
"log_BAEGarg2019_attack_BERT_all"   

The following two arguments are responsible for saving to checkpoints and saving the perturbed dataset:
```
log_to_csv=f"{root}/data/log_<attack_name>_{i}.csv",
checkpoint_dir=f"{root}/checkpoints_<attack_name>/{i}_checkpoints.csv",
```