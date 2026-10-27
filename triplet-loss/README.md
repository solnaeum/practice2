# Triplet Loss vs 원본 임베딩 (Fashion-MNIST)

- `triplet_vs_original_embedding.ipynb` — 원본 실습 노트북
- `triplet_vs_original_embedding.executed.ipynb` — 실행 결과 포함본 (CPU 4코어, torch 2.14.1, 약 8분)
- `figures/` — 실행 중 생성된 그림

## 결과 요약

| 임베딩 공간 | kNN 정확도 ↑ | 실루엣 ↑ | 클래스 내/간 거리 ↓ |
|---|---|---|---|
| 원본 픽셀 (784-d) | 0.773 | 0.042 | 0.757 |
| 학습 전 인코더 (64-d) | 0.641 | −0.085 | 0.785 |
| Triplet 학습 후 (64-d) | 0.891 | 0.496 | 0.379 |

30 에폭 동안 loss 0.274 → 0.128, active triplets 26.4% → 0.22%.
