# Implement your Own BERT
This is a code for developing a minimalist version of BERT.

In this project, I have implemented some important components of the BERT model to gain a better understanding its architecture. 
It then performs sentence classification on two datasets: the ``sst`` dataset and the ``cfimdb`` dataset with this BERT model.


python3 classifier.py --option [pretrain/finetune] --epochs NUM_EPOCHS --lr LR --train data/sst-train.txt --dev data/sst-dev.txt --test data/sst-test.txt
```

## Reference accuracies: 

Mean reference accuracies over 10 random seeds with their standard deviation shown in brackets.

Pretraining for SST:
Dev Accuracy: 0.391 (0.007)
Test Accuracy: 0.403 (0.008)

Finetuning for SST:
Dev Accuracy: 0.515 (0.004)
Test Accuracy: 0.526 (0.008)

Finetuning for CFIMDB:
Dev Accuracy: 0.966 (0.007)
Test Accuracy: -


files/
├── base_bert.py
├── bert.py
├── classifier.py
├── config.py
├── optimizer.py
├── sanity_check.py
├── tokenizer.py
├── utils.py
├── README.md
├── structure.md
├── sanity_check.data
├── sst-dev-output.txt 
├── sst-test-output.txt 
├── cfimdb-dev-output.txt 
├── cfimdb-test-output.txt 
└── setup.py
```

`prepare_submit.py` can help to create(1) or check(2) the to-be-submitted zip file. It will throw assertion errors if the format is not expected. Usage: (1) To create and check a zip file with your outputs, run `python3 prepare_submit.py path/to/your/output/dir folder_name`, (2) To check your zip file, run `python3 prepare_submit.py path/to/your/submit/zip/file.zip folder_name`



### Acknowledgements
_This project is adapted from the Carnegie Mellon University's CS11-711 course and the minBERT assignment created by Shuyan Zhou, Zhengbao Jiang, Ritam Dutt and Brendon Boldt._

Parts of the code are from the [`transformers`](https://github.com/huggingface/transformers) library ([Apache License 2.0](./LICENSE)).

