
# Open Image Classification Service (Bitcom)

People create images they wish to classify.

Various groups can classify images differently.

People prefer to pay for the best classification.

Classifiers can compete to provide the best tags
at the lowest price.

## Protocol


To request an image to be classified with tags
post a link to the image to the bitcom open
image classification bitcom.

```
ImageClassificationRequest {
  bitcom: string;
  linkType: string;
  link: string;
  reward_utxo_txid: string;
  reward_utxo_vout: number;
  signature: number;
}
```

Op Return Protocol:

```
<BITCOM> <LINK_TYPE> <LINK> <REWARD_UTXO> <SIGNATURE>
```

### BITCOM

Address of the bitcom program.

### LINK TYPE

- b
- ipfs
- http

### REWARD_UTXO

In format of `txid/vout` to indicate the coin

### REWARD_SIGNATURE

Proves ownership of the given coin

