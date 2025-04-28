# 🧠 Projeto Checkpoint 2 – Desenvolvimento de Sistema de Classificação Inteligente com MLP

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

**Exemplo de Soma dos RMs:**
- RM1 = 12345 → soma = 1+2+3+4+5 = 15
- RM2 = 54321 → soma = 5+4+3+2+1 = 15
- Soma total = 30
- Dataset OpenML a ser utilizado: ID 30 (se existir, senão usar o mais próximo).

---

## 📌 Critérios de Avaliação (Total: 10 pontos)

| Critério | Descrição | Pontos |
|:---------|:----------|:------|
| **1. Dataset selecionado/criado** | Escolha adequada do dataset (OpenML ou fictício) e coerência dos dados. | 2 pts |
| **2. Implementação correta com sklearn** | Uso correto da biblioteca `MLPClassifier`, divisão treino/teste, normalização dos dados. | 2 pts |
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
- Código em Python (`.ipynb`) bem comentado.
- Gráficos opcionais da evolução do erro ou acurácia (`matplotlib`).
- Relatório em `.pdf` ou `.md` (máximo 2 páginas).

---

## 📆 Prazo de Entrega
- A entrega deverá ser realizada até **o final da aula** após a liberação da proposta;
- Grupo de 5 integrantes e o representante entrega pelo portal.


