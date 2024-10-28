#   Counter-Narrative (CN) classifier in ReZG

This repository contains the training code and weights for the Counter-Narrative (CN) classifier used in Paper ```"ReZG: Retrieval-Augmented Zero-Shot Counter Narrative Generation for Hate Speech"```, which is used to determine the effectiveness of counter-narratives against hate speech. 

- **The training code** of it is in the file ```Finetune Roberta for CN detection.pynb```
- **The weight** of it is strored in ```CNClassifier-ReZG.pt```, which can be obtained through: https://pan.baidu.com/s/1c_iB2IgAiCyPCyviYucLPw?pwd=4q9x 

The training data is formalized as follows:

| index | target    | hs                                      | cn                                         | label |
|-------|-----------|-----------------------------------------|--------------------------------------------|-------|
| 1     | DISABLED | Folks with down syndrome are inferior.  | People with Down Syndrome are not inferior to anyone else.  Our genetic condition isn't something to be ashamed of, maybe we should be less judgemental about others. | 1     |
| 2     | DISABLED      | Folks with down syndrome are inferior. | All religions have value and are welcome to our country. | 0  |


- `index`: A unique identifier for each instance.
- `target`: The target of the hate speech.
- `hs`: The content of the hate speech (HS).
- `cn`: The text provided to challenge the hate speech.
- `label`: A binary label indicating whether the `cn` is a valid counter-narrative for the corresponding `hs`:
  - `1`: The `cn` is a valid counter-narrative for the `hs`.
  - `0`: The `cn` is not a valid counter-narrative for the `hs`.



The training data samples from the following studies and we would like to express our sincere thanks to them:
- [1] Chung, Yi-Ling, et al. "CONAN-COunter NArratives through Nichesourcing: a Multilingual Dataset of Responses to Fight Online Hate Speech." Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics. 2019.
- [2] Fanton, Margherita, et al. "Human-in-the-Loop for Data Collection: a Multi-Target Counter Narrative Dataset to Fight Online Hate Speech." Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (Volume 1: Long Papers). 2021.
- [3] Chung, Yi-Ling, Serra Sinem Tekiroğlu, and Marco Guerini. "Towards Knowledge-Grounded Counter Narrative Generation for Hate Speech." Findings of the Association for Computational Linguistics: ACL-IJCNLP 2021. 2021.
