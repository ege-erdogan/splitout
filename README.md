# SplitOut: Out-of-the-Box Training-Hijacking Detection in Split Learning via Outlier Detection


## Citation
```
@article{erdogan2023splitout,
  title={SplitOut: Out-of-the-Box Training-Hijacking Detection in Split Learning via Outlier Detection},
  author={Erdogan, Ege and Teksen, Unat and Celiktenyildiz, Mehmet Salih and Kupcu, Alptekin and Cicek, A Ercument},
  journal={arXiv preprint arXiv:2302.08618},
  year={2024}
}
```

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
