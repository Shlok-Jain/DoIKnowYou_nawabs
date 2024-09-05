# Nawabs' submission for "Do I know You?"
This is official submission for the problem statement "Do I know You?" by BCS, IITK for Takneek 2024 by pool "Nawabs".
Problem Statement: [Do I know You?](https://drive.google.com/file/d/1l3t1S5wo2yvOEyzMBMtHX1ttnGKQSheR/view)
# Team details
### Y22:
Aditya V
### Y23:

### Y24:

# Dataset details
- `anchored_terms.json`: This is the dataset used for implementing "Who is Harry Potter?" paper. This contains a dictionary of keywords specific to the RAW agents Wikipedia text and corresponding generic alternatives generated by ChatGPT.
- `forget_set_qna.json`: This is the dataset used for evaluating the model. It contains the question answer pairs which the model should forget after fine tuning.
- `world_facts.json`: This contains question-answer pairs containing general facts about the world (not related to RAW agents). This is used for evaluating how well model has remember world facts after fine tuning.
- `WikiTRUE.txt`: It contains the RAW agents Wikipedia text. It was used to train reinfored model required in "Who is Harry Potter?" paper.
- `WikiFALSE.txt`: This dataset contains which contains false information about RAW agents. It was used to fine tune the model to forget the data.


# Steps to run the code
1. Clone the repository
```bash
git clone https://github.com/Shlok-Jain/DoIKnowYou_nawabs.git
```
2. Change the directory
```bash
cd ./DoIKnowYou_nawabs
```

3. Run the code
### FineTuning
The file `QLora_finetune.ipynb` is in ipynb format, you will have to run all the cells to finetune the model, after installing the required libraries. The last cell is for pushing the model to huggingface repository.

### HellaSwag Evaluation
The file `HellaSwag.ipynb` is in ipynb format, you will have to run all the cells to evaluate the model, after installing the required libraries. It will evaluate the original model as well as fine tuned model.

### BLEU Score Evaluation
The file `BLEU_Score.ipynb` is in ipynb format. It takes the dataset of question answer pairs on the forget set, and generate answers using both the models (original and fine tuned). It then calculates the BLEU score between two. The lesser the BLEU score the greater it has learnt to forget the data.