# Zuber – Análise de Corridas e Impacto do Clima

Este projeto analisa dados de corridas de táxi em Chicago para a empresa **Zuber**, com o objetivo de identificar padrões de comportamento dos passageiros e avaliar o impacto de fatores externos — especialmente o clima — na duração e frequência das viagens.

---

## 🧪 Objetivo

Investigar:

- Quais empresas dominam o mercado em determinados períodos
- Quais bairros concentram mais destinos
- Como as condições climáticas impactam a duração das corridas
- Se há diferença estatística na duração das viagens em sábados chuvosos

O foco é combinar **consultas SQL, análise exploratória e testes de hipóteses em Python**.

---

## 🔍 Descrição do Projeto

O projeto está dividido em cinco etapas principais:

### 1️⃣ Análise de Dados Climáticos (Web Scraping)
- Coletar dados de clima de Chicago (novembro/2017) a partir de página HTML.
- Estruturar as informações para análise posterior.

### 2️⃣ Análise Exploratória (SQL)
Consultas ao banco de dados para:

- Número de corridas por empresa (15–16 nov 2017)
- Corridas de empresas com "Yellow" ou "Blue" no nome (1–7 nov 2017)
- Comparação entre Flash Cab, Taxi Affiliation Services e demais empresas
- Agrupamentos e ordenações estratégicas

### 3️⃣ Teste de Hipótese no Banco (SQL)
- Identificar bairros Loop e O'Hare
- Classificar condições meteorológicas como “Good” ou “Bad”
- Recuperar corridas do Loop para O'Hare em sábados
- Relacionar duração da corrida com condições climáticas

### 4️⃣ Análise Exploratória (Python)
Arquivos utilizados:
- `project_sql_result_01.csv`
- `project_sql_result_04.csv`

Atividades:
- Importação e inspeção dos dados
- Verificação de tipos de dados
- Identificação dos 10 principais bairros de destino
- Visualizações:
  - Empresas vs número de corridas
  - Top 10 bairros por média de corridas
- Interpretação dos resultados

### 5️⃣ Teste de Hipótese (Python)

Arquivo utilizado:
- `project_sql_result_07.csv`

Hipótese testada:
> A duração média das corridas do Loop para o Aeroporto O'Hare muda em sábados chuvosos.

Inclui:
- Formulação das hipóteses nula e alternativa
- Definição do nível de significância (alfa)
- Aplicação de teste estatístico apropriado
- Interpretação dos resultados

---

## 🚀 Tecnologias Utilizadas

- SQL (consultas e agregações)
- Python 3.11
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

> Bibliotecas adicionais estão listadas no `requirements.txt`.

---

## 📂 Estrutura dos Dados

Banco de dados com as seguintes tabelas:

| Tabela | Descrição |
|--------|-----------|
| `neighborhoods` | Bairros de Chicago |
| `cabs` | Dados dos veículos e empresas |
| `trips` | Informações das corridas |
| `weather_records` | Registros climáticos |

Arquivos CSV adicionais:
- `project_sql_result_01.csv`
- `project_sql_result_04.csv`
- `project_sql_result_07.csv`

---

## 📦 Como Executar

1. Clone o repositório:

```bash
git clone https://github.com/rodriguesbrian/tt7_zuber_project
cd tt7_zuber_project