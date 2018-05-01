# Chromium Conversations

#### A Dataset for Identifying Actionable Feedback in Collaborative Software Development

### Datasets

#### chromium_conversations.csv

This is the full dataset containing over 1.5 million comments posted by developers reviewing proposed code changes. The dataset also includes the values we calculated for all nine linguistic features (described in Section 4 of the paper cited below).

#### chromium_conversations_annotations.csv

This dataset is a subset of the `chromium_conversations.csv`  dataset. It contains the data used in the classification experiment outlined in Section 5 of the paper cited below (2,994 comments automatically identified as acted-upon and 800 comments manually identified as not (known-to-be) acted-upon).

#### Data Organization

| Column Name       | Description                                                                                                                                             |
|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| review_id         | Unique identifier of a code review in the Chromium project. The URL https://codereview.chromium.org/<review_id> may be used to access the review online |
| patchset_id       | Unique identifier of a code review patchset (i.e., collection of changes to the source code) associated with a review                                   |
| patch_id          | Unique identifier of a code review patch (i.e., individual change to the source code) associated with a patchset                                        |
| file_path         | The path to the file being modified in the patch                                                                                                        |
| line_number       | The line number in the file at which the comment was posted                                                                                             |
| posted_timestamp  | The timestamp indicating when the comment was posted                                                                                                    |
| author_email      | The (de-identified) author of the comment                                                                                                               |
| author_type       | The role of the author (i.e., reviewer or developer)                                                                                                    |
| text              | The raw natural language text of the code review comment                                                                                                |
| yngve             | The maximum Yngve score of sentences in the code review comment                                                                                         |
| frazier           | The maximum Frazier score of sentences in the code review comment                                                                                       |
| pdensity          | The Propositional Density score of the code review comment                                                                                              |
| cdensity          | The Content Density score of the code review comment                                                                                                    |
| pct_neg_tokens    | Ratio (percentage) of total number of tokens in negative sentences to the total number of tokens in all sentences in the code review comment            |
| pct_neu_tokens    | Ratio (percentage) of total number of tokens in neutral sentences to the total number of tokens in all sentences in the code review comment             |
| pct_pos_tokens    | Ratio (percentage) of total number of tokens in positive sentences to the total number of tokens in all sentences in the code review comment            |
| pct_nne_tokens    | Ratio (percentage) of total number of tokens in non-neutral sentences to the total number of tokens in all sentences in the code review comment         |
| min_politeness    | Minimum of the politeness of sentences in the code review comment                                                                                       |
| max_politeness    | Maximum of the politeness of sentences in the code review comment                                                                                       |
| min_formality     | Minimum of the formality of sentences in the code review comment                                                                                        |
| max_formality     | Maximum of the formality of sentences in the code review comment                                                                                        |
| num_tokens        | Total number of tokens in the code review comment                                                                                                       |
| num_sentences     | Total number of sentences in the code review comment                                                                                                    |
| has_doxastic      | Binary indicator of presence of a sentence with doxastic uncertainty in the code review comment                                                         |
| has_epistemic     | Binary indicator of presence of a sentence with epistemic uncertainty in the code review comment                                                        |
| has_conditional   | Binary indicator of presence of a sentence with conditional uncertainty in the code review comment                                                      |
| has_investigative | Binary indicator of presence of a sentence with investigative uncertainty in the code review comment                                                    |
| has_uncertainty   | Binary indicator of presence of a sentence with any uncertainty in the code review comment                                                              |
| comment_type      | Manual annotation of the type of code review comment between acted-upon and not (known to be) acted-upon                                                |


##### Citation

```
    A Dataset for Identifying Actionable Feedback in Collaborative Software Development.
        B.S. Meyers, N. Munaiah, E. Prud'hommeaux, A. Meneely, C.O. Alm, J. Wolff, and P.K. Murukannaiah.
        Proceedings of the 2018 Meeting for the Association for Computational Linguistics (ACL).
```

[Link]().
