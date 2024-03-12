## Generation Improving Fine Tuning
This repository shares code implementing various fine-tuning methodologies aimed at enhancing the generation capabilities of natural language generation model. 
There are four methodologies in total: **Standard**, **Auxiliary**, **Recurrent**, and **Generative**. 
Detailed descriptions of each methodology, along with their basic setups and performance evaluations in machine translation, are provided below.
<br><br>

## Fine-Tuning Strategy
**Standard** <br> 
> Standard Fine Tuning is the most common method of fine-tuning. 
It involves taking the parameters of a pre-trained model and applying the same training process as usual, but with a reduced learning rate for fine adjustments.

<br>

**Auxiliary** <br> 
> The Auxiliary strategy is a method that reduces the risk of exposure bias by using First Token Prediction as an auxiliary training objective alongside Maximum Likelihood Estimation (MLE), which serves as the main training objective.

<br>

**Recurrent** <br> 
> The Recurrent approach is a fine-tuning method inspired by Schedule Sampling for Transformer, where the output of the decoder is recursively utilized as input to the decoder.
However, unlike the Scheduled Sampling typically used in RNN Seq2Seq, the key difference lies in exclusively replacing all input values with the output of the decoder.

<br>

**Generative** <br> 
> The Generative method is a fine-tuning approach that incorporates generation during the training process by applying a certain proportion of the inference generation methodology.

<br><br>

## Setups
| Dataset | Model | Training |
|---|---|---|
| WMT14 En-De | Transformer Seq2Seq | Num of Epoch: 10 |

<br><br>

## Results
| Strategy | Score | Epoch Time | Avg GPU | Max GPU |
|:---:|---|---|---|---|
| BaseLine |||||
| Standard |||||
| Auxiliary |||||
| Recurrent |||||
| Generative |||||

<br><br>


## How to Use
**Clone repo on your local env**
```
git clone
```
<br> 

**Setup Dataset and Tokenizer**
```
python3 setup.py
```
<br> 

**Actual Process via run.py file**
```
python3 run.py -mode     [train, finetune, test, inference]
               -strategy [standard(default), auxiliary, recurrent, generative]
               -search   [beam, greedy]
```
<br><br>

## Reference
* **Attention is all you need**
* **Scheduled Sampling for Transformers**
<br>
