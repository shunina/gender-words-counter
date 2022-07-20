# gender_words_counter
gender_words_counter is created by Shun Inagaki, who is a student at Master of Computer Science at University of York. This is completely private software and only used for the research.

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
・japanese_gender_word_counter
- count the gendered words in Japanese job advertisements
・english_gender_word_counter
- count the gendered words in English job advertisements

## Directories
─ src
├ data
  ├gender_words_lists
    ├ en 
      ├feminine.json      : English feminine words
      └masculine.json     : English masculine words
    └ ja
      ├feminine.json      : Japanese feminine words
      └masculine.json     : Japanese masculine words
  ├ job_advertisements
    ├ en
      ├ cleaned           : cleaned English job advertisements
        ├beautician.json
        └・・・.json
      ├wikijob            : raw data and fetched data of wikijob's job advertisements
        ├wikijob.json
        └wikijob.xml
      ├beautician.json    : raw data of find a job's job advertisements
      └・・・.json
    └ ja
      ├ cleaned           : cleaned Japanese job advertisements
        ├beautician.json
        └・・・.json
      ├beautician.json    : raw data of rikunabi's job advertisements
      └・・・.json
  ├ results               : results of gendered words count for job advertisements(data are included in rawdata.zip's result directory)
      ├english_gendered_words_in_advertisements.csv
      ├english_result_per_occupation.csv
      ├english_result.csv
      ├japanese_gendered_words_in_advertisements.csv
      ├japanese_results_per_occupation.csv
      └japanese_result.csv
  ├english_job_advertisements_cleaner.ipynb
  ├english_gender_word_counter.ipynb
  ├find_a_job.ipynb
  ├japanese_gender_word_counter.ipynb
  ├japanese_job_advertisements_cleaner.ipynb
  ├rikunabi.ipynb
  └wikijob.ipynb
※Data are not included in this directory. They are included in rawdata.zip in the artefact directory.

## Environment
python 3 environment (recommend to use Python 3.10.0 and jupyter notebook)

## Installation
install mecab
```macOS
brew install mecab
brew install mecab-ipadic
```

install mecab-ipadic-NEologd 
```macOS(m1 chip)
cd src
git clone --depth 1 https://github.com/neologd/mecab-ipadic-neologd.git
cd mecab-ipadic-neologd
./bin/install-mecab-ipadic-neologd -n -a
```

install python libraries (please install other libraries if required depending on your local environment)
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
