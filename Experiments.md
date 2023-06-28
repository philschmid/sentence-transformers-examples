# First run 

```
python train_mnrl.py \
  --model_name bigcode/starpii \
  --train_batch_size 32 \
  --max_seq_length 300 \
  --max_passages 0 \
  --epochs 2 \
  --pooling mean \
  --negs_to_use None \
  --warmup_steps 1000 \
  --lr 2e-5 \
  --num_negs_per_system 5 \
  --negs_to_use bm25,msmarco-MiniLM-L-6-v3 \
  --ce_score_margin 3.0
```

eval on 100k

```
2023-06-28 11:32:48 - Score-Function: cos_sim
2023-06-28 11:32:48 - Accuracy@1: 67.66%
2023-06-28 11:32:48 - Accuracy@3: 79.74%
2023-06-28 11:32:48 - Accuracy@5: 83.95%
2023-06-28 11:32:48 - Accuracy@10: 88.52%
2023-06-28 11:32:48 - Precision@10: 9.29%
2023-06-28 11:32:48 - Precision@100: 1.02%
2023-06-28 11:32:48 - Recall@10: 87.78%
2023-06-28 11:32:48 - Recall@100: 96.03%
2023-06-28 11:32:48 - MRR@10: 0.7466
2023-06-28 11:32:48 - NDCG@10: 0.7741
2023-06-28 11:32:48 - MAP@100: 0.7418
2023-06-28 11:32:48 - Score-Function: dot_score
2023-06-28 11:32:48 - Accuracy@1: 65.79%
2023-06-28 11:32:48 - Accuracy@3: 78.24%
2023-06-28 11:32:48 - Accuracy@5: 82.87%
2023-06-28 11:32:48 - Accuracy@10: 87.16%
2023-06-28 11:32:48 - Precision@10: 9.13%
2023-06-28 11:32:48 - Precision@100: 1.02%
2023-06-28 11:32:48 - Recall@10: 86.35%
2023-06-28 11:32:48 - Recall@100: 95.75%
2023-06-28 11:32:48 - MRR@10: 0.7297
2023-06-28 11:32:48 - NDCG@10: 0.7578
2023-06-28 11:32:48 - MAP@100: 0.7254
```

# second run 

```bash
python train_mnrl.py \
  --model_name bigcode/starpii \
  --train_batch_size 32 \
  --max_seq_length 300 \
  --max_passages 0 \
  --epochs 10 \
  --pooling mean \
  --negs_to_use None \
  --warmup_steps 1000 \
  --lr 2e-5 \
  --num_negs_per_system 5 \
  --negs_to_use bm25,msmarco-MiniLM-L-6-v3 \
  --ce_score_margin 3.0
```