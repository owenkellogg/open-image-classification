
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

ImageClassification {
  bitcom: string;
  classificationRequestId: string;
  tags: string[];
}

```

Op Return Protocol:

```
<BITCOM> request <LINK_TYPE> <LINK> <REWARD_UTXO> <SIGNATURE>
```

```
<BITCOM> classify <REQUEST_TXID> <REWARD_ADDRESS> <tag1> [tag2] [tag3] [tag4] [tag5] ...

```

### BITCOM

Address of the bitcom program: 1DvCuEXrXtUhmxiHFx1Smq7Zk2FWh3KkCQ

### LINK TYPE

- b
- ipfs
- http

### REWARD UTXO

In format of `txid/vout` to indicate the coin

### REWARD SIGNATURE

Proves ownership of the given coin

### REQUEST TXID

Reference to transaction that requested image classification

### REWARD ADDRESS

Address to which the reward will be send when accepted

