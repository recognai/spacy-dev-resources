# Scripts for building vocabulary from a corpus

## Install dependencies

Run `fab -f vocab/fabfile install_dep` which will install the necessary python packages, downloads and install the Brown clustering script.

## Usage

To create vocabulary files from Wikipeda run the following command from the root directory

`fab -f vocab/fabfile build_wiki_vocab:<lang>`

In case you already have a corpus, you can also build a vocabulary using your data by running

`fab -f vocab/fabfile build_vocab:<lang>,<corpus_files_root>` (where `corpus_files_root` directory contains plain text files)

Your vocabulary is placed at `./data/model/<lang>/vocab`, now you can build your language model using [spaCy's CLI](https://spacy.io/docs/usage/cli#package)