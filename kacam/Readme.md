# KACAM

Implementation of Knowledge-aware Attentive Compare-Aggregate Model on TrecQA and WikiQA using Keras.

## Requirements

* python 3.x
* Keras 2.2.4
* Tensorflow 1.12.0

## Data

* WikiQA
* TrecQA

## Preprocess

Because the data file is too large, it is not uploaded here. I will give a download link to the original data and preprocessing data after publication. The details of the preprocessing are in ```preprocess.py```.

## Running

```
usage: main.py [-h] [-t Task] [-m MODEL] [-d HIDDEN_DIM] [-e PATIENCE] [-l LR] [-b BATCH_SIZE] [--no_entity_cmp] [--no_cxt_weight_mixed] [--no_ent_weight_mixed]
```

### WikiQA

* KACAM

```
python main.py -t wikiqa
```

* w/o att_cxt

```
python main.py -t wikiqa --no_ent_weight_mixed
```

* w/o att_ent

```
python main.py -t wikiqa --no_cxt_weight_mixed
```

* w/o att_cxt_ent

```
python main.py -t wikiqa --no_cxt_weight_mixed --no_ent_weight_mixed
```

* w/o ent_fea

```
python main.py -t wikiqa --no_entity_cmp
```

* w/o ent

```
python main.py -t wikiqa --no_entity_cmp --no_cxt_weight_mixed
```

### TrecQA

It's similar to WikiQA, change task from 'wikiqa' to 'trecqa'. For example:

```
python main.py -t trecqa
```

## References

```
@inproceedings{bian2017compare,
  title={A compare-aggregate model with dynamic-clip attention for answer selection},
  author={Bian, Weijie and Li, Si and Yang, Zhao and Chen, Guang and Lin, Zhiqing},
  booktitle={Proceedings of the 2017 ACM on Conference on Information and Knowledge Management},
  pages={1987--1990},
  year={2017},
  organization={ACM}
}

@inproceedings{shen2018knowledge,
  title={Knowledge-aware attentive neural network for ranking question answer pairs},
  author={Shen, Ying and Deng, Yang and Yang, Min and Li, Yaliang and Du, Nan and Fan, Wei and Lei, Kai},
  booktitle={The 41st International ACM SIGIR Conference on Research \& Development in Information Retrieval},
  pages={901--904},
  year={2018},
  organization={ACM}
}
```

