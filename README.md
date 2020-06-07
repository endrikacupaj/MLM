# MLM

## About

Multiple Languages and Modalities (MLM) is a dataset consisting of text in three languages (EN, DE, FR), images, location data, and triple classes.
The resource is designed to evaluate multitask learning systems that conducts the following core tasks:
- Information retrieval (IR)
- Location estimation (LE)

IR+LE is an architecture for a baseline multitask learning system with two objectives to learn on multiple modalities and languages. The pipeline for IR extends a system proposed by Marin et al for cross-modal retrieval:
http://im2recipe.csail.mit.edu/im2recipe-journal.pdf


## Set Up
### Requirements and Setup
Python version >= 3.7

PyTorch version >= 1.4.0

``` bash
# clone the repository
git clone https://github.com/GOALCLEOPATRA/MLM.git
cd MLM
pip install -r requirements.txt
```

### Download MLM dataset

Download the dataset hdf5 files from [here](https://zenodo.org/record/3822551) and place them under the [data](data) folder.

### Train tasks
Multi-task Learning (IR & LE)
``` bash
python train.py --task mtl
```

Information retrieval task
``` bash
python train.py --task ir
```

Location estimation task
``` bash
python train.py --task le
```

For providing other arguments (e.g. epochs, batch size, dropout) please check [args.py](args.py).

### Test tasks
Multi-task Learning (IR & LE)
``` bash
python test.py --task mtl
```

Information retrieval task
``` bash
python test.py --task ir
```

Location estimation task
``` bash
python test.py --task le
```

All logs and checkpoints will be saved under the experiments folder.

### Files for location and scene embeddings

https://tib.eu/cloud/s/SWNckCMgdxSMXR7

## License
The repository is under [MIT License](LICENSE).

## Cite
``` bash
Coming Soon!
```
