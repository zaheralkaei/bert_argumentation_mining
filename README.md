# Argumentation Mining with BERT  
By Zaher Alkaei

This project fine-tunes a BERT model to classify argumentative components—**Claim**, **Premise**, and **Non-argumentative (O)**—in US presidential campaign debate transcripts. It includes preprocessing, fine-tuning with class weighting, evaluation, and model explainability using Integrated Gradients.

## Dataset  
**Source**: [Yes, we can! Mining Arguments in 50 Years of US Presidential Campaign Debates (Haddadan et al., ACL 2019)](https://github.com/ElecDeb60To16/Dataset)

## Labels  
- `O`: Non-argumentative  
- `Claim`  
- `Premise`  

## Features  
- Uses `bert-base-uncased` from Hugging Face Transformers  
- Applies class weights to handle label imbalance  
- Trains using `Trainer` API with early stopping  
- Evaluates using standard classification metrics  
- Visualizes token importance using Captum (Integrated Gradients)  

## How to Run  
This notebook is designed for Google Colab. To run locally:  
1. Install required packages
2. Place your dataset as sentence_db_candidate.csv in the working directory.
3. Run the notebook cells step-by-step.

## Output
Fine-tuned model saved in ./bert_argument_model

Classification report on test set

Token-level attribution scores by predicted class

## License
This code is for academic and research use. Refer to the dataset’s repository for its usage terms.
