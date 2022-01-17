# SentiMP-21 Dataset

The SentiMP-21 Dataset is a multilingual sentiment analysis dataset based on tweets written by members of parliament in Greece, Spain and United Kingdom in 2021.  It has been developed collaboratively by the [Andalusian Research Institute in Data Science and Computational Intelligence (DaSCI)](https://dasci.es/) research  group from the [University of Granada](https://www.ugr.es/) and the [Cardiff NLP](https://sites.google.com/view/cardiffnlp/) research group from the [University of Cardiff](https://isc.cardiff.ac.uk/).

<p align="center"><img src="https://sherpa-cdn.s3-eu-west-1.amazonaws.com/third_parties_logos/DaSCI_logo_vertical.png"  alt="Andalusian Research Institute in Data Science and Computational Intelligence" height = "240"/>
<img src="https://upload.wikimedia.org/wikipedia/commons/e/ef/Cardiff_University_%28logo%29.svg" alt="Sherpa AI" height = "210" /></p>

## Dataset details

The dataset containst 1500 tweets from three different countries: Greece (500 tweets), Spain (500 tweets) and United Kingdom (500 tweets). For each tweet we provide the following information:
* **tweet_id**: Which represents the identifier of each tweet.
* **full_text**: Which containts the content of the tweet.
* **mp_party**: Party to which the member of parliament who wrote the tweet belongs.
* **mp_name**: Name of the member of parliament who wrote the tweet.
* **created_at**: Date of the tweet.
* **label_i** : Annotator's i label (i in {1,2,3} for English and Greek and i in {1,2,3,4,5} for Spanish). It takes values in {-1,0,1,x}.
* **majority_vote**: The result after applying the majority vote strategy to the annotators' partial labelling. When there is a tie we use the label "TIE". It takes values in {-1,0,1,TIE}.
* **tie_break**:  We use this column to break ties in cases where there is a tie. Therefore, it is only completed when TIE appears in the *majority_vote* column. It takes values in {-1,0,1}.
* **final_label**: It represents the final label. It is a combination between the *majority_vote* abd the *tie_break* columns. It takes values in {-1,0,1}.

## Downloads

We release three different version for each of the datasets:

* Extended version (full): We include all the columns for each of the initial 500 tweets.
* Extended version (without x): We delete the tweets labeled with "x" from the previous version.
* Simple version: It only keeps the columns *tweet_id*, *full_text* and *final_label* from the previous version.

You can find these files in the following repositories:
* [Spain dataset](./sp/)
* [UK dataset](./uk/)
* [Greece dataset](./gr/)

## Citation
If you use this dataset, please cite:


## Contact
Nuria Rodríguez Barroso - rbnuria@ugr.es


Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
