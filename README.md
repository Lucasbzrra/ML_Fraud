# Projeto "ML_Fraud"

Desenvolvi o projeto **"ML_Fraud"**, com o objetivo de prever possíveis fraudes em transações de cartão de crédito utilizando aprendizado de máquina. Este projeto foi estruturado em etapas claras, desde a análise inicial dos dados até a criação de um modelo robusto para detecção de fraudes.

## Etapas do Projeto

### 1. **Análise e Tratamento de Dados**
A primeira etapa consistiu na verificação e tratamento do conjunto de dados. Realizei limpeza, manipulação e criação de novas features para enriquecer o conjunto de dados, utilizando técnicas de Análise Exploratória de Dados (EDA). Exemplos de features criadas incluem:
- **`Income_per_Profession`**: Renda do indivíduo em relação à média da profissão.
- **`Above_Avg_Income`**: Indicador binário para rendas acima da média por profissão.
- **`Income_Category`**: Classificação categórica de renda em "Baixo", "Médio" e "Alto".
- **`Income_per_Age`**: Renda proporcional à idade.

Além disso, utilizei **One-Hot Encoding** para transformar variáveis categóricas, como "Profissão", e adaptei os dados para entrada nos modelos.

### 2. **Divisão e Seleção de Dados**
Realizei a separação do conjunto de dados em features (`X`) e rótulo (`y`) — sendo este último a variável alvo de detecção de fraudes. Em seguida, dividi o conjunto em dados de treino e teste (80%/20%) e implementei validação cruzada estratificada para garantir a robustez do treinamento.

### 3. **Modelos Utilizados**
Utilizei os seguintes algoritmos de aprendizado de máquina para realizar as predições:
- **Regressão Logística**
- **Árvore de Decisão**
- **Floresta Aleatória**

A escolha e o ajuste dos hiperparâmetros foram feitos utilizando **GridSearchCV** com validação cruzada aninhada, garantindo uma avaliação justa e confiável dos modelos.

### 4. **Treinamento e Avaliação**
O modelo de Regressão Logística foi ajustado com os seguintes melhores hiperparâmetros:
```python
print("Melhores hiperparâmetros:", lr_gs.best_params_)
