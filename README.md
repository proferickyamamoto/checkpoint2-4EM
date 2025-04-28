# 🧠 Projeto Avaliativo – Desenvolvimento de Sistema de Classificação Inteligente com MLP

## 🎯 Objetivo
Desenvolver um sistema usando **MLP (Multilayer Perceptron)** que classifique dados personalizados, integrando teoria e prática de Redes Neurais. O projeto deverá utilizar informações baseadas na **soma dos RM dos integrantes do grupo** para criar características únicas.

---

## 📩 Descrição do Projeto
Cada grupo deverá:
- Criar seu **próprio conjunto de dados** OU utilizar um **dataset real do OpenML** baseado no **valor final da soma dos dígitos dos RMs**.
- Treinar uma **MLP personalizada** utilizando `sklearn`.
- Criar também uma **implementação própria** de uma MLP simples (sem usar bibliotecas prontas como `sklearn` para o modelo).
- Avaliar e comparar os resultados.

---

## 🧩 Regras específicas
- A **quantidade de neurônios ocultos** será igual à soma dos dígitos dos RMs.
- O **dataset** será selecionado do OpenML pelo ID correspondente à soma final.
- Caso o ID do OpenML não exista ou seja impraticável, o grupo poderá criar um dataset fictício.
- Cada entrada deve ter **entre 3 e 5 atributos**.
- Utilizar **função de ativação** `ReLU` na camada oculta e `Softmax` ou `Sigmoid` na saída.

**Sobre o OpenML:**
- Site: [https://www.openml.org/](https://www.openml.org/)
- Pesquisar o dataset pelo número do ID.

### 📜 Exemplo de código para carregar o dataset do OpenML:

```python
# Instalar openml caso não tenha
# pip install openml

import openml

# Substitua pelo ID correspondente à soma dos RMs
dataset_id = 30

dataset = openml.datasets.get_dataset(dataset_id)
X, y, _, _ = dataset.get_data(target=dataset.default_target_attribute)

print("Shape das entradas:", X.shape)
print("Primeiras entradas:")
print(X.head())
print("Primeiros rótulos:")
print(y.head())
```

---

## 📌 Critérios de Avaliação (Total: 10 pontos)

| Critério | Descrição | Pontos |
|:---------|:----------|:------|
| **1. Dataset selecionado/criado** | Escolha adequada do dataset (OpenML ou fictício) e coerência dos dados. | 2 pts |
| **2. Implementação correta com sklearn** | Uso correto da biblioteca `MLPClassifier` ou `MLPRegressor`, divisão treino/teste, normalização dos dados. | 2 pts |
| **3. Implementação própria de MLP** | Construção de uma rede simples em Python, com feedforward e treinamento (gradiente descendente). | 3 pts |
| **4. Comparação de resultados** | Análise crítica comparando a implementação própria com o sklearn. | 2 pts |
| **5. Organização e clareza** | Código limpo, bem comentado e entrega estruturada. | 1 pt |

---

## 📦 O que deve conter na entrega
- Cálculo da soma dos RMs e indicação do dataset escolhido.
- Breve descrição do problema modelado.
- Implementação do modelo com `sklearn`.
- Implementação de uma MLP simples manualmente.
- Comparativo de acurácia/erro entre os dois modelos.
- Código em Python (`.ipynb` ou `.py`) bem comentado.
- Gráficos opcionais da evolução do erro ou acurácia (`matplotlib`).
- Relatório em `.pdf` ou `.md` (máximo 2 páginas).

---

## 📆 Prazo de Entrega
- A entrega deverá ser realizada até final da aula após a liberação da proposta;
- Grupo de até 7 integrantes e o representante entrega pelo portal.
