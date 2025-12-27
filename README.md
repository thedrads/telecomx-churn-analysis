# 📊 TelecomX - Análise de Evasão de Clientes

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.2+-green?logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-success)
![License](https://img.shields.io/badge/License-MIT-blue)

> **Challenge de Data Science | Alura + Oracle Next Education (ONE)**

Análise completa de churn (evasão de clientes) da empresa TelecomX, seguindo processo ETL rigoroso e preparação para Machine Learning.

---

## 📑 Índice

- [📊 Sobre o Projeto](#-sobre-o-projeto)
- [🎯 Objetivos](#-objetivos)
- [📁 Estrutura do Repositório](#-estrutura-do-repositório)
- [🚀 Como Reproduzir](#-como-reproduzir)
- [📊 Principais Descobertas](#-principais-descobertas)
- [💡 Insights Estratégicos](#-insights-estratégicos)
- [🤖 Preparação para ML](#-preparação-para-ml)
- [📚 Tecnologias](#-tecnologias)
- [👨‍💻 Autor](#-autor)
- [📄 Licença](#-licença)

---

## 📊 Sobre o Projeto

A **TelecomX** é uma empresa de telecomunicações que enfrenta um desafio crítico: **alto índice de cancelamento de contratos** (churn de 25.7%). Este projeto analisa dados de **7.043 clientes** para identificar padrões e gerar insights acionáveis para redução de evasão.

### 🎯 Metodologia

O projeto seguiu o framework **ETL (Extract, Transform, Load)** com análise exploratória completa:
```
┌─────────────┐      ┌─────────────┐      ┌─────────────┐      ┌─────────────┐
│   EXTRACT   │ ───> │  TRANSFORM  │ ───> │    LOAD     │ ───> │     EDA     │
│             │      │             │      │             │      │             │
│ • API REST  │      │ • Limpeza   │      │ • CSV       │      │ • 10 Gráfs  │
│ • JSON      │      │ • Tradução  │      │ • Validado  │      │ • Insights  │
│ • 7.3k rows │      │ • Validação │      │ • ML-ready  │      │ • ML Prep   │
└─────────────┘      └─────────────┘      └─────────────┘      └─────────────┘
```

### 🔧 Diferenciais do Projeto

- ✅ **Colunas traduzidas para português** (facilita compreensão e ML)
- ✅ **ETL rigoroso** com análise profunda de 224 valores vazios
- ✅ **Decisões documentadas** com justificativas estatísticas
- ✅ **10 análises visuais** seguindo boas práticas (sem gráficos de pizza)
- ✅ **Dataset preparado para ML** (tipos corretos, 0 missing values)
- ✅ **Insights priorizados** por impacto no negócio

---

## 🎯 Objetivos

| Objetivo | Status |
|----------|--------|
| Extrair dados via API REST | ✅ Concluído |
| Limpar e transformar dados (ETL) | ✅ Concluído |
| Identificar padrões de churn | ✅ Concluído |
| Gerar insights acionáveis | ✅ Concluído |
| Preparar dataset para ML | ✅ Concluído |
| Documentar todo o processo | ✅ Concluído |

---

## 📁 Estrutura do Repositório
```
telecomx-churn-analysis/
│
├── notebooks/
│   └── analise_churn_telecom.ipynb    # Notebook principal (33 células)
│
├── data/
│   └── processed/
│       └── telecom_limpo.csv          # Dataset limpo final (7.043 × 21)
│
├── docs/                               # Documentação adicional
│
├── README.md                           # Este arquivo
├── requirements.txt                    # Dependências Python
├── LICENSE                             # Licença MIT
└── .gitignore                         # Arquivos ignorados
```

### 📥 Acesso aos Arquivos

#### 📓 Notebook Completo
- **GitHub:** [notebooks/analise_churn_telecom.ipynb](notebooks/analise_churn_telecom.ipynb)
- **Google Colab:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thedrads/telecomx-churn-analysis/blob/main/notebooks/analise_churn_telecom.ipynb)

#### 📊 Dataset Limpo (CSV)
- **GitHub:** [data/processed/telecom_limpo.csv](data/processed/telecom_limpo.csv)
- **URL Direta:** `https://raw.githubusercontent.com/thedrads/telecomx-churn-analysis/main/data/processed/telecom_limpo.csv`

---

## 🚀 Como Reproduzir

### 1️⃣ Clonar o Repositório
```bash
git clone https://github.com/thedrads/telecomx-churn-analysis.git
cd telecomx-churn-analysis
```

### 2️⃣ Instalar Dependências
```bash
pip install -r requirements.txt
```

### 3️⃣ Executar o Notebook

**Opção A: Google Colab (Recomendado)**
- Clique no badge acima [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thedrads/telecomx-churn-analysis/blob/main/notebooks/analise_churn_telecom.ipynb)
- Runtime → Run all

**Opção B: Local (Jupyter)**
```bash
jupyter notebook notebooks/analise_churn_telecom.ipynb
```

### 4️⃣ Carregar Dataset Pronto (Opcional)

Pular ETL e carregar CSV direto:
```python
import pandas as pd

url = "https://raw.githubusercontent.com/thedrads/telecomx-churn-analysis/main/data/processed/telecom_limpo.csv"
df = pd.read_csv(url)

print(f"✅ Dataset: {len(df):,} registros × {len(df.columns)} colunas")
```

---

## 📊 Principais Descobertas

### 📉 Situação Atual

| Métrica | Valor | Comparação |
|---------|-------|------------|
| **Taxa de Churn** | 25.7% | 🔴 Acima da média do setor (15-20%) |
| **Clientes Perdidos** | 1.813 | - |
| **Perda Mensal** | $120.961 | - |
| **Perda Anual** | **$1.45 milhões** | 🔴 Crítico |

### 🔴 Fatores de Alto Risco

| Fator | Taxa de Churn | Diferença | Criticidade |
|-------|---------------|-----------|-------------|
| **Contratos Mensais** | 43% | +32pp vs anuais | 🔴 Muito Alta |
| **Primeiros 12 meses** | 47% | +38pp vs 48+ meses | 🔴 Muito Alta |
| **Idosos (65+)** | 41.7% | +17pp vs não-idosos | 🔴 Alta |
| **Fibra Óptica** | 42% | +23pp vs DSL | 🟡 Alta |
| **Sem Dependentes** | 31% | +15pp vs com | 🟡 Média |

### 🟢 Fatores Protetores

| Fator | Taxa de Churn | Redução | Impacto |
|-------|---------------|---------|---------|
| **Contratos Bianuais** | 3% | -40pp vs mensais | 🟢 Excelente |
| **Contratos Anuais** | 11% | -32pp vs mensais | 🟢 Muito Bom |
| **Tempo > 48 meses** | 9% | -38pp vs 0-12 meses | 🟢 Muito Bom |
| **Com Dependentes** | 16% | -15pp vs sem | 🟢 Bom |
| **Sem Internet** | 7% | -35pp vs Fibra | 🟢 Bom |

---

## 💡 Insights Estratégicos

### 1️⃣ Contratos Mensais: O Maior Risco 🔴

**Descoberta:** Clientes com contratos mensais têm churn **10x maior** que bianuais (43% vs 3%)

**Ação Recomendada:**
- ✅ Campanha de migração com desconto de 15% para contratos anuais
- ✅ Meta: Converter 30% em 6 meses
- ✅ ROI esperado: ~$400K/ano

---

### 2️⃣ Primeiros 12 Meses: Período Crítico 🔴

**Descoberta:** 47% do churn acontece nos **primeiros 12 meses** de contrato

**Ação Recomendada:**
- ✅ Programa de onboarding intensivo (primeiros 3 meses)
- ✅ Check-ins mensais automatizados
- ✅ Benefícios progressivos de fidelidade

---

### 3️⃣ Idosos Precisam de Atenção Especial 🟡

**Descoberta:** Idosos (65+) têm **17pp a mais** de churn (41.7% vs 23.6%)

**Ação Recomendada:**
- ✅ Equipe de suporte dedicada para idosos
- ✅ Tutorial simplificado de serviços
- ✅ Desconto para aposentados (5-10%)

---

### 4️⃣ Paradoxo da Fibra Óptica 🟡

**Descoberta:** Serviço **premium** (Fibra Óptica) tem **maior churn** (42%)

**Ação Recomendada:**
- ✅ Pesquisa urgente de satisfação
- ✅ Benchmarking de preço vs. concorrência
- ✅ Auditoria técnica de qualidade

---

### 5️⃣ Família = Lealdade 🟢

**Descoberta:** Clientes com vínculos familiares cancelam **15pp menos**

**Ação Recomendada:**
- ✅ Criar planos familiares com desconto (10-15%)
- ✅ Adicionar linhas adicionais gratuitas
- ✅ Benefícios compartilhados

---

## 🤖 Preparação para ML

### ✅ Dataset 100% Pronto para Modelagem

**Características:**
- ✅ **7.043 registros** (após limpeza rigorosa)
- ✅ **21 variáveis** (4 numéricas, 17 categóricas)
- ✅ **0 valores nulos**
- ✅ **0 duplicados**
- ✅ **Tipos corretos** (int64, float64, object)
- ✅ **Variável alvo validada** (cancelou: Yes/No)
- ✅ **Colunas em português**

### 📊 Variáveis Mais Importantes

Baseado em análise de correlação e crosstabs:

| Ranking | Variável | Correlação/Impacto | Importância ML |
|---------|----------|---------------------|----------------|
| 1 | `tipo_contrato` | Churn varia 3% a 43% | 🔴 Muito Alta |
| 2 | `meses_cliente` | -0.352 | 🔴 Muito Alta |
| 3 | `cobranca_mensal` | +0.193 | 🟡 Alta |
| 4 | `idoso` | +0.150 | 🟡 Alta |
| 5 | `tipo_internet` | Churn varia 7% a 42% | 🟡 Alta |

### 🎯 Modelos Recomendados

1. **Logistic Regression** - Baseline interpretável
2. **Random Forest** - Equilíbrio performance/interpretabilidade
3. **XGBoost** - Melhor performance

**Métricas críticas:** Precision, **Recall** (prioridade), F1-Score, AUC-ROC

---

## 📚 Tecnologias

### 🐍 Stack Principal

| Tecnologia | Versão | Uso |
|------------|--------|-----|
| **Python** | 3.10+ | Linguagem base |
| **Pandas** | 2.2+ | Manipulação de dados |
| **NumPy** | 2.0+ | Operações numéricas |
| **Matplotlib** | 3.10+ | Visualização estática |
| **Seaborn** | 0.13+ | Visualização estatística |
| **Plotly** | 5.18+ | Visualização interativa |

---

## 👨‍💻 Autor

**Fábio Andrade**

- 🐙 GitHub: [@thedrads](https://github.com/thedrads)
- 💼 LinkedIn: [Fábio Andrade](https://linkedin.com/in/seu-perfil)
- 📧 Email: [Fábio Andrade](fabiodandrade@uol.com.br)

---

## 📄 Licença

Este projeto está sob a licença **MIT**. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 🙏 Agradecimentos

- **Alura** - Pela estruturação do Challenge e conteúdo de qualidade
- **Oracle ONE** - Pelo apoio ao programa Next Education
- **Comunidade Data Science** - Pelas discussões e aprendizados contínuos

---

⭐ **Se este projeto foi útil, deixe uma estrela no repositório!** ⭐

---

<p align="center">
  Desenvolvido com 💼 e ☕ por <strong>Fábio Andrade</strong><br>
  <sub>Challenge de Data Science | Alura + Oracle ONE | 2025</sub>
</p>

---
