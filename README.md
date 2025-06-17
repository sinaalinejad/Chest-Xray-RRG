# Chest-Xray-RRG

## Contributors

### Author

- Sina Alinejad

### Supervisor

- Dr.Sauleh Eetemadi

## Abstract

In this study, we propose a model for generating radiology reports for chest X-ray images. Automatic report generation is crucial due to the high volume of imaging requests and the shortage of radiologists. Such models can assist radiologists by facilitating faster and more accurate detection of abnormalities. We first introduce a baseline Report-Augmented Generation (RAG) model that generates reports by retrieving similar past reports. Then, we propose an enhanced model, Feature and Report Augmented Generation (FRAG), which retrieves not only past reports but also relevant clinical features or abnormalities associated with the input image. These retrieved elements are jointly used during the report generation process. The FRAG model is implemented in two variants: FRAG-A, which employs a zero-shot inference module, and FRAG-B, which utilizes a linear classifier for abnormality detection. All models are evaluated using both medical and natural language metrics. Evaluation results demonstrate that FRAG models significantly outperform the baseline RAG model in clinical metrics, with FRAG-A showing superior performance. Additionally, we conduct further experiments to examine the effect of the retrieval strategy, large language model, and prompting used in the generation stage. The ELIXR-B vision-language model is used for retrieval, and after embedding extraction, three selection strategies—top-k, K-Means clustering, and maximally diverse selection—are explored. The findings reveal that both the retrieval method and the choice of language model substantially impact performance, whereas the prompt template has a minimal effect.

## 📚 Overview

This project addresses an image captioning problem where the model should generate a textual report for chest x-ray radiology images.

## Dataset


## Classes

| Abnormality                                 | Description                                                                 |
|---------------------------------------------|-----------------------------------------------------------------------------|
| Atelectasis                                 | Lack of a well-defined inheritance structure where one is needed.           |
| Cardiomegaly                                | Methods or functions with too many parameters, making them hard to use.     |
| Consolidation                               | Abstractions that add no clear benefit or are not justified in the context. |
| Edema                                       | Abstractions that enforce imperative logic, reducing flexibility.           |
| Pleural Effusion                            | Catch blocks that fail to handle exceptions, leading to silent failures.    |
| Pneumonia                                   | Poorly protected data, exposing internal details unnecessarily.             |
| Pneumothorax                                | Excessively lengthy names for variables, methods, or classes.               |
| Enlarged Cardiom.                           | Classes or interfaces with too many responsibilities.                      |
| Lung Lesion                                 | Inheritance trees that are too broad, making navigation difficult.          |
| Lung Opacity                                | Conditional expressions that are hard to read or understand.                |
| Pleural Other                               | Inheritance structures that violate logical or expected relationships.      |
| Fracture                                    | Use of literal numbers without explanation, reducing code clarity.          |
| Support Devices                             | Switch statements lacking a default case, risking unhandled scenarios.      |


## Code

## Methods

## 🛠️ Setup Instructions


## 📊 Evaluation Results

The results of the code smell detection evaluation on various models are shown in Table 1. These models were trained for one epoch on 10,000 data points with a maximum input length of 3,000 tokens, using AdamW as the optimizer and binary cross-entropy as the loss function.

| Model             |   Bleu-1  |  Bleu-3 | Rouge-L  | S_emb   | Macro F1 | Micro F1|
|-------------------|-----------|---------|----------|---------|----------|---------|
| RAG               | 88.78%    | 61.39%  | 85.95%   | 72.59%  |  45.25   |  74.52  |


## Future Work


## Conclusion
