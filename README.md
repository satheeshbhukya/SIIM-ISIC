# SIIMA ISIC MELANOMA CLASSIFICATION 

# Identify melanoma in lesion images. 

I used EfficientNet [B0-B6], Resnest,Resnext, with Sizes 192x192 256x256 384x384 512x512 768x768 384x512[HxW] 

# What Worked for me: 

- Heavy TTA (X20)
- Cutmix
- Coarse dropout
- SWA(Stochastic Weight Averaging)
- Loss-Label Smoothing, BCE
- Optimizers - AdamW, Adam
- 2018, 2020 and malignant datasets
- 5 checkpoints' prediction averaging(stabalised our model's predictions)
- some models were trained with different height width ratios 

# Ensembling Techniques:

- Weighted average
- Power Average
- Minmax ensemble(didn't help) 

# Result : 

15+ pytorch model (with context) and 15+ tf models (without context) - The metric used was ROC
AUC and score was 0.9470
