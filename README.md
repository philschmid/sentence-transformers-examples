# Train Sentence Transformers

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

# Evaluate Sentence Transformers

```
python eval.py model_name [max_corpus_size_in_thousands]
```

```
python eval.py output/train_bi-encoder-mnrl-bigcode-starpii-margin_3.0-2023-06-28_07-22-45 100
```