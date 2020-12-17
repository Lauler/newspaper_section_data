# Dataset of classified newspaper section identifiers in Svenska Dagbladet 2003-2019

The purpose of this repository is to share (meta)data and predictions from a project classifying section identifiers in digitized newspapers. The paper describing the process has not been published yet. In the meantime the reader is referred to [Rekathati (2020)](http://urn.kb.se/resolve?urn=urn:nbn:se:liu:diva-166313). The dataset is intended for researchers with access to API and resources at The National Library of Sweden's [KBLab](https://www.kb.se/in-english/research-collaboration/kblab.html).

## Description

A zipped .7z archive containing 3 files: `design3.parquet`, `design4.parquet`, `design5.parquet`. Each file corresponds to a specific design period of the newspaper (see referenced thesis above for details).


| Variable  | Description |
| ------------- | ------------- |
| id  | The URI for the observation. Acts as unique identifier and links to API. |
| cosine_similarity_5 | A similarity search was performed using a reference image of a section identifier (for example SPORTS). The most similar observations' corresponding images were printed to a folder sorted in order of most similar to least similar. Human annotators cleaned/deleted images which did not contain the section identifier featured in the reference image. The cleaning was performed until a stopping criterion was met: "stop when 5 images in a row do not contain the section identifier class found in the reference image". |
| cosine_similarity_10  | "Stop when 10 images in a row do not contain the section identifier class of the reference image" |
| cosine_similarity_15  | "Stop when 15 images in a row do not contain the section identifier class of the reference image" |
| label_xgboost  | Raw predictions from xgboost model |
| probability  | Confidence of xgboost model in the prediction |
| label_xgboost_adjusted | Xgboost predictions reviewed and corrected by human annotators |
| training_set | Observations used to train the Xgboost model |
| evaluation_set | Observations used as evalution set |


## Download

[Download link](https://kungliga-biblioteket.box.com/s/7q70d4bz7bpq47i0km8yznpywkks9pqa)
