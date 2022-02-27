# gender_words_counter
gender_words_counter is created by Shun Inagaki, who is a student at Master of Computer Science at University of York. This repository is completely private and only used for the research.

## Feature
・find_a_job
- web scraper to get job advertisement data from Find A Job (https://findajob.dwp.gov.uk/)
・rikunabi
- web scraper to get job advertisement data from rikunabi (https://next.rikunabi.com/)
・wikijob
- get job advertisement data of wikijob by Feed url and parse them to convert to the data 
・english_advertisement_cleaner
- clean the sentences in English job advertisements before the calculation process of gender scores
・japanese_advertisement_cleaner
- clean the sentences in Japanese job advertisements before the calculation process of gender scores

## Environment
python 3 environment (recommend to use 3.10.0 jupyter notebook)

## Installation
install mecab
```macOS
brew install mecab
brew install mecab-ipadic
```

install mecab-ipadic-NEologd 
```macOS(m1 chip)
git clone --depth 1 https://github.com/neologd/mecab-ipadic-neologd.git
cd mecab-ipadic-neologd
./bin/install-mecab-ipadic-neologd -n -a
```

install python libraries
```bash
pip install requests
pip install beautifulsoup4
pip install neologdn
pip install import-ipynb
pip install wheel
pip install mecab-python3
pip install pandas
pip install numpy
```
