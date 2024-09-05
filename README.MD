# Nawabs' submission for "Do I know You?"
This is official submission for the problem statement "Do I know You?" by BCS, IITK for Takneek 2024 by pool "Nawabs".
Problem Statement: [Do I know You?](https://drive.google.com/file/d/1l3t1S5wo2yvOEyzMBMtHX1ttnGKQSheR/view)
# Team details
### Y22:

### Y23:

### Y24:

# Steps to run the code
1. Clone the repository
```bash
git clone 
```
2. Change the directory
```bash
cd ./
```

3. Run the code
### FineTuning
The file `QLora_finetune.ipynb` is in ipynb format, you will have to run all the cells to finetune the model, after installing the required libraries. The last cell is for pushing the model to huggingface repository.

### HellaSwag Evaluation
The file `HellaSwag.ipynb` is in ipynb format, you will have to run all the cells to evaluate the model, after installing the required libraries. It will evaluate the original model as well as fine tuned model.

### BLEU Score Evaluation
The file `BLEU_Score.ipynb` is in ipynb format. It takes the dataset of question answer pairs on the forget set, and generate answers using both the models (original and fine tuned). It then calculates the BLEU score between two. The lesser the BLEU score the greater it has learnt to forget the data.