# 🍷 Dataset Wine (sklearn)

O dataset **Wine** é um conjunto de dados clássico de classificação, amplamente utilizado para fins educacionais e testes de modelos.

## 📋 Descrição Geral

- **Objetivo**: Classificar vinhos em 3 categorias com base em suas características químicas.
- **Tarefa**: Classificação multiclasse (target com 3 classes: 0, 1 e 2)
- **Número de amostras**: 178 vinhos
- **Número de features**: 13 variáveis contínuas

## 🧪 Variáveis (Features)

As 13 variáveis representam propriedades químicas do vinho, como:

- `alcohol`: teor alcoólico
- `malic_acid`: ácido málico
- `ash`: teor de cinzas
- `alcalinity_of_ash`: alcalinidade das cinzas
- `magnesium`: teor de magnésio
- `total_phenols`: fenóis totais
- `flavanoids`: flavonoides
- `nonflavanoid_phenols`: fenóis não-flavonoides
- `proanthocyanins`: proantocianidinas
- `color_intensity`: intensidade de cor
- `hue`: matiz
- `od280/od315_of_diluted_wines`: índice de absorção
- `proline`: teor de prolina

## 🏷️ Target

- `0`: Vinho da classe 0
- `1`: Vinho da classe 1
- `2`: Vinho da classe 2

Essas classes representam **três cultivares diferentes** de vinho originados da região italiana.

## 📦 Como carregar

```python
from sklearn.datasets import load_wine
data = load_wine()
df = pd.DataFrame(data.data, columns=data.feature_names)
df['target'] = data.target
