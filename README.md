# MurTree Data Repository

This repository contains input dataset files that can be used with [MurTree](https://github.com/MurTree/murtree) and [pymurtree](https://github.com/MurTree/pymurtree).

The datasets are benchmarks from other papers, binarised with the _continuousToCategorical.r_ R script included in this repository. Each subdirectory contains data from one paper. The papers are as follows:

- DL  -  Aglin, Gaël; Siegfried Nijssen; Pierre Schaus. _"Learning optimal decision trees using caching branch-and-bound search."_ (AAAI'20).

- NL  -  Verwer, Sicco; Yingqian Zhang. _"Learning optimal classification trees using a binary linear program formulation."_ (AAAI'19).

- Nina  -  Narodytska, Nina; Ignatiev, Alexey; Pereira, Filipe; Marques-Silva, Joao. _"Learning Optimal Decision Trees with SAT."_ (IJCAI'18).

- Hu  -  Hu, Xiyang; Cynthia Rudin; Margo Seltzer. _"Optimal sparse decision trees."_ (NeurIPS'19).


## Usage

To use these datasets, clone this repository or download the desired files, and specify the file paths as input when running MurTree.

For example, to run MurTree using the dataset in _anneal.txt_:

```sh
git clone git@github.com:MurTree/murtree-data.git
./murtree -file murtree-data/DL/anneal.txt -max-depth 4 -max-num-nodes 15 -time 600
```

## File format

- The data files are in plain text format.

- Each line is one instance. The first number is the label while the rest are features.

- All features zero-one. Labels are integers starting from zero. Non-binarised instances must be converted into binary form, e.g., using the binarisation script _continuousToCategorical.r_ included in this repository.

## License
This repository is licensed under the MIT License. See the LICENSE file for details.
