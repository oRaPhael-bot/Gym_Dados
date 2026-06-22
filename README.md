# Gym_Dados
Projeto de Dados sobre uma base de dados de uma academia.

# 🏋️‍♂️ Dashboard de Análise de Desempenho e Saúde (Gym Members Tracking)

![Capa do Projeto](<img width="963" height="506" alt="image" src="https://github.com/user-attachments/assets/72312d16-e429-4b25-a49f-8e0773335199" />
)

## 📌 Contexto do Projeto
Este projeto de **Power BI** foi desenvolvido para analisar o comportamento, o esforço físico e o perfil de saúde dos membros de uma academia. 

O objetivo principal deste dashboard é responder a perguntas de negócio focadas em gestão esportiva e saúde: **Quais tipos de treino são mais eficientes para a queima calórica? Como a experiência e a biometria dos alunos impactam o desempenho e os hábitos saudáveis?**

🔗 **[Acesse o Dashboard Interativo Aqui] (Insira o link de publicação do Power BI)**

## 📊 Estrutura dos Dados
A base de dados utilizada contém detalhes de sessões de treino de centenas de membros. As principais métricas analisadas incluem:

* **Perfil Físico:** Idade, Gênero, Peso, Altura, IMC (*BMI*) e Percentual de Gordura (*Fat_Percentage*).
* **Esforço e Desempenho:** Calorias Queimadas, Duração da Sessão (horas) e Frequência Cardíaca (BPM Máximo, Médio e em Repouso).
* **Hábitos de Treino:** Tipo de Treino (*Yoga, HIIT, Cardio, Strength*), Frequência Semanal, Consumo de Água (litros) e Nível de Experiência (1 a 3).

## 💡 Principais Insights e Análises
Ao desenvolver o painel, os dados revelaram padrões muito interessantes sobre os alunos:

1. **Correlação entre Esforço Cardíaco e Queima Calórica:** O cruzamento de dados mostra que sessões com BPM médio elevado resultam em altíssima queima calórica. [cite_start]Em um dos registros de Cardio, um aluno queimou **1.385 kcal** em uma sessão de apenas **1.49 horas**, mantendo um BPM médio de **169**[cite: 1].
2. **Impacto do Nível de Experiência nos Hábitos:** Existe uma divisão clara no engajamento. [cite_start]Alunos com **Nível de Experiência 3 (Avançado)** treinam frequentemente de **4 a 5 dias por semana** e chegam a consumir **3.5 litros de água** diários[cite: 1].
3. [cite_start]**Comportamento dos Iniciantes:** Em contrapartida, membros classificados com **Nível de Experiência 1 (Iniciante)** apresentam um consumo de água mais tímido (girando em torno de **1.6 a 2.8 litros**) e uma frequência média menor, frequentando a academia cerca de **2 a 3 vezes na semana**[cite: 1].
4. [cite_start]**Eficiência do Tempo de Treino:** Mesmo em treinos mais curtos (abaixo de 1 hora), alunos que praticam modalidades de força (*Strength*) ou HIIT conseguem manter picos de queima calórica acima de **500 kcal** quando o esforço cardiovascular é mantido[cite: 1].

## 🛠️ Ferramentas e Técnicas Utilizadas
* **Power Query (Linguagem M):** * Tratamento da base de dados e tipagem correta de decimais (Peso, Altura, IMC, Litros de água).
  * Criação de colunas condicionais para categorização de IMC (Ex: Abaixo do peso, Normal, Sobrepeso).
* **DAX (Data Analysis Expressions):**
  * Criação de medidas explícitas para cálculo de médias e proporções. Exemplo de medida criada para analisar a eficiência do treino:
    ```dax
    Queima Calórica por Hora = 
    DIVIDE(
        SUM('Base'[Calories_Burned]), 
        SUM('Base'[Session_Duration (hours)])
    )
    ```
* **Modelagem de Dados:** Estruturação lógica separando atributos descritivos e valores numéricos em tabelas Fato e Dimensão para otimizar a performance do dashboard.
* **Data Visualization:** Utilização de Gráficos de Dispersão (Scatter Plots para cruzar BPM x Calorias), Gráficos de Barras para Tipos de Treino e Cartões de KPI para médias de saúde.

## 📂 Como navegar neste repositório
- `\dados`: Contém o arquivo `.csv` original utilizado na análise.
- `\imagens`: Prints das telas principais (Visão Geral, Análise de Esforço e Perfil de Saúde).
- `Dashboard_Academia.pbip`: Arquivo do projeto Power BI salvo em formato *Project* para visualização da estrutura.

---
Feito com 💡 e análise de dados por **[Seu Nome/Seu LinkedIn]**.
