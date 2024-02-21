# Zero-One-Few-Shot Question Answering
M.Sc. in Language Technology M915-NLG_NLU Assignment2: Development and Comparison of N-shot QA systems on [SQuAD v.1](https://huggingface.co/datasets/squad) with a pretrained generative language model.

This is a useful repo for you to experiment with the zero one and few sgot learning scheme on Question answering with the use of LLMs. Here, [Flan-T5 Small](https://huggingface.co/docs/transformers/model_doc/flan-t5) is used, due to its reported few shot capabilities.

# Prompt template
![image](https://github.com/Kleo-Karap/QA_systems/assets/117507917/f0fbbfae-c3b3-4931-8d73-859026c4457a)

# Experiment settings and results
1. Zero-shot: no instructions
2. One-shot: Single use of prompt template
3. Few-shot: Random 9-shots after finetuning
4. Exp_Few-shot: 11-shots from Question classification in 11 question types ("What", "How many", "How", "Whom", "Whose", "Who", "When", "Which", "Where", "Why", "Be/Do/etc., "Other"}

Evaluation on the official dev set with typical QA metrics: [Exact Match](https://huggingface.co/spaces/evaluate-metric/exact_match) and [F1_score](https://kierszbaumsamuel.medium.com/f1-score-in-nlp-span-based-qa-task-5b115a5e7d41) 
![image](https://github.com/Kleo-Karap/QA_systems/assets/117507917/18070e38-faec-4aff-84e4-357ee5a61a29)

# Contributor Expectations
- Increase the window size between k-value of shots (e.g 10-20-30) to check for bigger differences in evaluation metrics
- Instead of random sampling, use k-demonstrations of one single Wikipedia article (e.g Super Bowl, Nikola_Tesla or any other specific document) in order to if the model learns more patterns in one specific document and learns to discern 
  pattterns based on the posed quedstion. (Pay Attention to overfitting!)
- Try larger versions of Flan T5 or any other LLM (e.g a decoder only model like BART)  
