# SplitOut: Out-of-the-Box Training-Hijacking Detection in Split Learning via Outlier Detection

## Citation
```
@article{erdougan2024splitout,
  title={SplitOut: Out-of-the-Box Training-Hijacking Detection in Split Learning via Outlier Detection},
  author={Erdogan, Ege and Teksen, Unat and Celiktenyildiz, Mehmet Salih and Kupcu, Alptekin and Cicek, A Ercument},
  booktitle={International Conference on Cryptology and Network Security},
  pages={118--142},
  year={2024},
  organization={Springer}
}
```

## Abstract

Split learning enables efficient and privacy-aware training of a deep neural network by splitting a neural network so that the clients (data holders) compute the first layers and only share the intermediate output with the central compute-heavy server. This paradigm introduces a new attack medium in which the server has full control over what the client models learn, which has already been exploited to infer the private data of clients and to implement backdoors in the client models. Although previous work has shown that clients can successfully detect such training-hijacking attacks, the proposed methods rely on heuristics, require tuning of many hyperparameters, and do not fully utilize the clients' capabilities. In this work, we show that given modest assumptions regarding the clients' compute capabilities, an out-of-the-box outlier detection method can be used to detect existing training-hijacking attacks with almost-zero false positive rates. We conclude through experiments on different tasks that the simplicity of our approach we name _**SplitOut**_ makes it a more viable and reliable alternative compared to the earlier detection methods.

**Cryptology and Network Security (CANS 2024):** https://doi.org/10.1007/978-981-97-8016-7_6
https://arxiv.org/abs/2302.08618

## How to Run 

Make sure that all files in the same directory:
- models.py
- sg_ad.ipynb
- util.py

### Requirements

Make sure you have the following libraries installed:

```
numpy
torch
torchvision
scipy
tqdm
matplotlib
pandas
```

### Running


#### 1. Upload Collected Gradients
start executing the `sg_ad.ipynb` notebook. Before running the detection mechanism, ensure you upload your collected gradients to the following path from the cell under the header `1) Loading FSHA and honest gradients`:
```
drive_path = '/content/drive/MyDrive/grads'
```

#### 2. Start Running SplitOut
Continue with executing the notebook from the cell under the header `3) Converting Tensor gradients to NumPy Array`. 

#### 3. Update SplitOut Parameters
Adjust the following parameters in the notebook to fit your needs from `4) Selecting desired reduced data rate` and continue executing all cells until the end of the notebook.

- data_rate_honest_gradients 
- window_size_list

## Updates

**24.06.2024:** Our code is released.
**01.10.2024:** Our paper is published in [**Cryptology and Network Security. CANS 2024. Lecture Notes in Computer Science**](https://link.springer.com/chapter/10.1007/978-981-97-8016-7_6).
