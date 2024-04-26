# Published Paper
Related published paper can be found here:
https://aclanthology.org/2023.arabicnlp-1.82/

Cite it as follows:
```
@inproceedings{zekiye-amroush-2023-al,
    title = "Al-Jawaab at Qur{'}an {QA} 2023 Shared Task: Exploring Embeddings and {GPT} Models for Passage Retrieval and Reading Comprehension",
    author = "Zekiye, Abdulrezzak  and
      Amroush, Fadi",
    editor = "Sawaf, Hassan  and
      El-Beltagy, Samhaa  and
      Zaghouani, Wajdi  and
      Magdy, Walid  and
      Abdelali, Ahmed  and
      Tomeh, Nadi  and
      Abu Farha, Ibrahim  and
      Habash, Nizar  and
      Khalifa, Salam  and
      Keleg, Amr  and
      Haddad, Hatem  and
      Zitouni, Imed  and
      Mrini, Khalil  and
      Almatham, Rawan",
    booktitle = "Proceedings of ArabicNLP 2023",
    month = dec,
    year = "2023",
    address = "Singapore (Hybrid)",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.arabicnlp-1.82",
    doi = "10.18653/v1/2023.arabicnlp-1.82",
    pages = "743--747",
}
```

# Readme for Task A and Task B

This repository contains two Python Notebooks for performing natural language processing tasks on Arabic text using OpenAI's GPT-4 model and embedding vectors. Each script has its own specific functionality and requirements. Below, you'll find a brief description of each script and how to use them. Codes to evaluate the submissions and datasets can be found from the official competition website (https://sites.google.com/view/quran-qa-2023).

**We achieved as the second place in Task B.**

Note: The code is not optimal and there might be some fractions that are not used or libraries which are imported but not used as well.

## Task A

### Description
The `Task A` script uses the OpenAI Embeddings API to compute document embeddings and rank passages by their similarity to the input questions. Many parts of Task A codes can be found from OpenAI's official website.

### Requirements
- Python 3.7 or higher
- Several Python libraries are required and can be installed using `pip`:
  - `arabic-reshaper`
  - `pytrec_eval`
  - `openai`
  - `tiktoken`
  - `numpy`
  - `pandas`
  
### Usage
1. Make sure you have installed all the required libraries mentioned above.
2. Set your OpenAI API key by replacing `'YOUR_OPENAI_API_KEY'` in the script with your actual API key.
3. Execute the script.

The script reads Quranic passages from the `QQA23_TaskA_QPC_v1.1.tsv` file, computes document embeddings for each passage, and retrieves the most relevant passages for each question. The results are saved in a file named `AlJawaab_emb.tsv`. You can change the file name of the dev file to be the test or the training one.

## Task B

### Description
The `Task B` script uses the OpenAI GPT-4 model to generate answers to questions based on the provided passages.

### Requirements
- Python 3.7 or higher
- Several Python libraries are required and can be installed using `pip`:
  - `pyarabic`
  - `tiktoken`
  - `farasapy`
  - `openai`
  - `numpy`
  - `pandas`

### Usage
1. Make sure you have installed all the required libraries mentioned above.
2. Set your OpenAI API key by replacing `'YOUR_OPENAI_API_KEY'` in the script with your actual API key.
3. Ensure that you have the dataset file (`QQA23_TaskB_qrcd_v1.2_test_preprocessed.jsonl`) in the same directory as the script.
4. Execute the script.
 
You can change the file name of the dev file to be the test or the training one.

The script reads questions and passages from the dataset file, sends questions to the GPT-4 model, and retrieves answers. It then saves the answers in a structured format.

Please note that both scripts require a working OpenAI API key for access to the GPT-4 model.
