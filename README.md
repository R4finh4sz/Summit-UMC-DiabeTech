
# 🧠 Impacto da Escolha da Validação Cruzada no Desempenho de SVM para Diagnóstico de Diabetes  

Repositório para apresentação no **Summit 2025 da Universidade UMC**, contendo código, análises e resultados referentes ao estudo sobre o impacto da escolha de diferentes esquemas de validação cruzada no desempenho de um classificador **SVM (Support Vector Machine)**, utilizando o dataset **Pima Indians Diabetes Database**.

---

## 📌 Contexto  

O uso de algoritmos de **aprendizado de máquina** na área biomédica requer estratégias de validação robustas para garantir a confiabilidade dos resultados. Neste projeto, investigamos como diferentes técnicas de **validação cruzada** afetam a performance de um modelo SVM aplicado ao diagnóstico de diabetes.  

---

## 🎯 Objetivo  

Comparar o desempenho do SVM utilizando dois esquemas de validação cruzada:  

- **KFold-10** (10 folds, sem estratificação)  
- **ShuffleSplit (30%, N = 10)** – 30% dos dados usados como teste em cada split aleatório  

As métricas analisadas foram:  
- **Acurácia média**  
- **Matriz de confusão**  

---

## 📊 Resultados  

| Método           | Acurácia Média | Observações |
|------------------|--------------|-------------|
| **KFold-10**     | 76,56%       | Tendência a mais **falsos negativos** |
| **ShuffleSplit** | 77,40% (±2,6) | Distribuição mais variável de **FP/FN** entre os splits |

> 🔎 **Insight principal:**  
Apesar da acurácia média ser semelhante, o tipo de validação impacta a consistência na classificação de casos minoritários, algo crítico para aplicações clínicas.  

---

## 🚀 Como Rodar no Google Colab  

Você pode executar este projeto diretamente no **Google Colab**, sem precisar instalar nada localmente.  

### 1️⃣ Abrir o Colab  
Acesse: [https://colab.research.google.com](https://colab.research.google.com)

### 2️⃣ Carregar o Notebook  
1. Clique em **Arquivo > Fazer upload de notebook**  
2. Envie o arquivo `Notebook_.ipynb`  

### 3️⃣ Instalar Dependências no Colab  
No início do notebook, adicione e execute a seguinte célula:  

```python
!pip install scikit-learn pandas numpy matplotlib
```

### 4️⃣ Executar o Código  
Agora basta rodar as células do notebook sequencialmente e verificar as métricas e matrizes de confusão geradas.

---

## 📂 Estrutura do Repositório  

```
.
├── /img                     #Graficos
├── /doc                     # Documentação do projeto e o Poster utilizado
├── Notbook_.ipynb 
│
└── README.md
```

---

## 🏆 Conclusões  

- A escolha do esquema de validação cruzada influencia não apenas a métrica global de acurácia, mas também a **distribuição dos erros**.  
- Para datasets desbalanceados, **KFold-10** tende a produzir resultados mais consistentes, enquanto **ShuffleSplit** pode apresentar maior variabilidade.  
- Este achado reforça a importância de **documentar e justificar** a escolha do método de validação em estudos biomédicos.  

---

## 👥 Equipe  

- **[Graziela Pereira de Oliveira, Gustavo Di Risio, Iago Lucas Fernandes De Faria, Rafael Souza Santana, Rayane Da Luz Barbosa]** – Pesquisador/Desenvolvedor  
- **[Fabiano Menegidio]** – Orientador  
- **Universidade UMC** – Summit 2025  
