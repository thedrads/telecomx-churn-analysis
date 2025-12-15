# TelecomX – Análise de Evasão de Clientes (Churn)

## Visão Geral

Este projeto apresenta uma **análise exploratória de dados (EDA)** focada na evasão de clientes (**churn**) da empresa fictícia **TelecomX**, com o objetivo de identificar **padrões, fatores críticos e insights acionáveis** para apoiar decisões estratégicas de retenção.

O trabalho foi desenvolvido com foco em **qualidade de dados, clareza analítica e aderência a boas práticas**, sem utilização de modelos preditivos, conforme o escopo definido.

---

## Objetivo do Projeto

* Analisar o comportamento de churn dos clientes
* Identificar fatores associados à evasão
* Explorar relações entre churn e variáveis:
  * Contratuais
  * Comportamentais
  * Financeiras
* Gerar insights claros para apoio à tomada de decisão

---

## Escopo e Limitações

* ✔️ Extração, tratamento e análise exploratória de dados
* ✔️ Visualizações e estatísticas descritivas
* ❌ Não inclui modelagem preditiva
* ❌ Não inclui deploy de modelos ou APIs

---

## Tecnologias Utilizadas

* **Python 3**
* **Pandas** – manipulação e transformação de dados
* **NumPy** – suporte a operações numéricas
* **Matplotlib / Seaborn** – visualização de dados
* **Jupyter Notebook** – ambiente de análise
* **Git & GitHub** – versionamento e controle de código

---

## Metodologia

### 1. Extração de Dados

* Dados obtidos via API em formato **JSON**
* Fonte versionada e reprodutível

### 2. Transformação e Limpeza (ETL)

* Normalização de estruturas aninhadas
* Padronização de nomes de colunas
* Conversão de tipos de dados
* Tratamento de valores ausentes
* Preservação semântica de categorias relevantes
  (ex.: *“No Internet Service”*)

### 3. Análise Exploratória de Dados (EDA)

* Estatísticas descritivas
* Análise da variável-alvo (*churn*)
* Visualizações comparativas entre grupos
* Identificação de padrões e tendências

---

## Principais Insights

* **Contratos Month-to-month** apresentam maior taxa de churn
* **Contratos de longo prazo** (One year / Two year) reduzem fortemente a evasão
* Clientes com **menor tempo de permanência (tenure)** têm maior probabilidade de churn
* **Mensalidades mais altas** estão associadas a maior evasão
* **Electronic check** é o método de pagamento com maior concentração de churn
* Pagamentos **automáticos** estão ligados a maior retenção

---

## Estrutura do Repositório

telecomx-churn-analysis/
│
├── README.md
├── notebooks/
│   └── telecomx.ipynb
├── index.html
└── .gitignore

---

## Como Executar o Projeto Localmente

### Pré-requisitos

* Python 3.10+
* Ambiente virtual (opcional, mas recomendado)

### Passos

# Clone o repositório
git clone https://github.com/thedrads/telecomx-churn-analysis.git

# Acesse a pasta do projeto
cd telecomx-churn-analysis

# Instale as dependências principais
python -m pip install pandas numpy matplotlib seaborn jupyter

# Execute o notebook
jupyter notebook notebooks/telecomx.ipynb

---

## Visualização Online do Relatório

O relatório final em HTML pode ser acessado via **GitHub Pages**:

🔗 [https://thedrads.github.io/telecomx-churn-analysis/](https://thedrads.github.io/telecomx-churn-analysis/)

---

## Resultados e Conclusões

A análise demonstra que o churn na TelecomX está fortemente relacionado a **fatores contratuais, financeiros e comportamentais**, indicando que estratégias focadas em:

* Incentivo a contratos de longo prazo
* Promoção de pagamentos automáticos
* Ações de retenção nos primeiros meses do cliente

podem gerar impacto relevante na redução da evasão.

---

## Autor

**Fábio Andrade**

Gestor Financeiro e Operacional | Transição para Dados, IA e Cloud
Projeto desenvolvido para fins educacionais e de portfólio profissional.

---

### Status do Projeto

✔️ Concluído
✔️ Pronto para avaliação e apresentação
✔️ Publicável como portfólio
* Criar uma **versão resumida** do projeto para portfólio
* Padronizar esse README como **template para próximos projetos**
