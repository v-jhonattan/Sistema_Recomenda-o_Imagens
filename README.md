
## Sistema de recomendação que encontra produtos visualmente similares (cor, forma, textura) sem usar metadados textuais.
- Arquitetura leve, 100% CPU:
- Embeddings: CLIP (ViT-B/32, via open_clip_torch)
- Índice ANN: Annoy (métrica angular ≈ cosseno)
- Classificação opcional: linear head sobre os embeddings (para 4 classes)
- Classes usadas no exemplo: watches, tshirts, bikes, sneakers.

## 🎯 Objetivo
- Dado um produto (imagem), retornar Top-K itens visualmente similares do catálogo.
- Semelhantes por aparência (não por marca/modelo/preço).
