# 🌸 Projeto IA Preditiva - Classificação Iris

Este projeto demonstra o uso de **aprendizado de máquina (Machine Learning)** com **árvores de decisão (Decision Tree)** para classificar flores do conjunto de dados *Iris Dataset*.  
O foco é mostrar de forma prática como treinar, testar e usar modelos preditivos salvos em arquivos `.pkl`.

---

## 📂 Estrutura do Projeto

| Arquivo | Descrição |
|----------|------------|
| **ia-preditiva.ipynb** | Notebook principal do projeto. Contém todo o código de treinamento, teste e avaliação dos modelos preditivos. |
| **Iris.csv** | Base de dados usada para treinar e testar os modelos. Inclui medidas de sépalas e pétalas das espécies Iris Setosa, Versicolor e Virginica. |
| **modelo_iris_DecisionTree_Gini.pkl** | Modelo treinado com o algoritmo *Decision Tree* usando o critério **Gini**. Específico para o dataset Iris. |
| **modelo_class_DecisionTree_Gini.pkl** | Modelo genérico de classificação baseado em *Decision Tree* com Gini. Pode ser reutilizado para outros conjuntos de dados. |

---

## 🚀 Como Funciona

1. O arquivo `Iris.csv` é carregado no notebook.  
2. O código realiza o **pré-processamento** dos dados (limpeza e separação em treino/teste).  
3. O modelo é treinado com o **DecisionTreeClassifier (criterion='gini')**.  
4. Após o treino, o modelo é **salvo em um arquivo `.pkl`** para uso futuro sem precisar reentreinar.  
5. Os modelos `.pkl` podem ser carregados novamente para **fazer previsões automáticas**.

---

## 🧠 Objetivo

Demonstrar de forma simples:
- Como usar o algoritmo Decision Tree;
- Como salvar e reutilizar modelos (`.pkl`);
- Como aplicar aprendizado supervisionado em dados reais.

---

## 🧩 Tecnologias Utilizadas

- Python  
- Pandas  
- Scikit-learn  
- Matplotlib / Seaborn  
- Jupyter Notebook  

---

## 🪄 Exemplo de Uso

```python
import pickle
import pandas as pd

# Carrega o modelo
with open('modelo_iris_DecisionTree_Gini.pkl', 'rb') as arquivo:
    modelo = pickle.load(arquivo)

# Exemplo de previsão
amostra = [[5.1, 3.5, 1.4, 0.2]]
previsao = modelo.predict(amostra)

print("Espécie prevista:", previsao[0])
```

---

## ✍️ Autor

**Vitor Maciel**  
Projeto desenvolvido como exemplo prático de *IA preditiva e classificação supervisionada.*

---

## 📘 Licença

Este projeto é de uso livre para fins educacionais e demonstração.
