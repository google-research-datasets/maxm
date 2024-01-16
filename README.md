# MaXM

<p align="center">
  <img width="360" height="600" src="/images/maxm_examples.png">
</p>

We introduce MaXM, a test-only multi-lingual visual question answering benchmark in 7 diverse languages: English (en), French (fr), Hindi (hi), Hebrew (iw), Romanian (ro), Thai (th), and Chinese (zh).
The datasets are based on the images and the captions from the [Crossmodal-3600](https://google.github.io/crossmodal-3600/) dataset (XM3600).
Check our [paper](https://arxiv.org/abs/2209.05401) for further details.

Our approach to data generation is similar to [VQ^2A](https://arxiv.org/abs/2205.01883) used to generate [MAVERICS](https://github.com/google-research-datasets/maverics).

<p align="center">
  <img width="458" height=250" src="/images/maxm_approach.png">
</p>

## Download

[MaXM v1](https://storage.googleapis.com/maxm/maxm_v1_release.zip) (157KB, released on Feb 18, 2023)


**Format (.json)**
<div class="highlight highlight-source-shell"><pre>
dataset                 str: dataset name
version                 str: dataset version
split                   str: language ID
annotations             List of image-question-answers triplets, each of which is
-- image_id             str: image ID
-- image_url            str: image URL
-- qa_pairs             List of question-answer pairs, each of which is
---- question_id        str: question ID
---- question           str: raw question
---- answers            List of str: ground-truth answers
---- processed_answers  List of str: processed ground-truth answers. 16 tokenized answers.
---- is_collection      bool: "true" if the question is of the "Collection" type; "false" otherwise..

</pre></div>

## Cite

If you use this dataset in your research, please cite the original Crossmodal-3600 dataset and our paper:

Soravit Changpinyo, Linting Xue, Michal Yarom, Ashish V. Thapliyal, Idan Szpektor, Julien Amelot, Xi Chen, Radu Soricut.
[MaXM: Towards Multilingual Visual Question Answering](https://arxiv.org/abs/2209.05401).
Findings of the Association for Computational Linguistics: EMNLP, 2023.

<div class="highlight highlight-source-shell"><pre>
@inproceedings{changpinyo2023maxm,
  title = {{MaXM}: Towards Multilingual Visual Question Answering},
  author = {Changpinyo, Soravit and Xue, Linting and Yarom, Michal and Thapliyal, Ashish V. and Szpektor, Idan and Amelot, Julien and Chen, Xi and Soricut, Radu},
  booktitle={Findings of the Association for Computational Linguistics: EMNLP},
  year = {2023},
}
</pre></div>

## Contact Us

Please create an issue in this repository. If you would like to share feedback or report concerns, please email schangpi@google.com.

