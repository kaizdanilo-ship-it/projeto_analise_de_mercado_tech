# 📊 Análise do Mercado de Trabalho em Tecnologia — Brasil (2024-2026)

> Projeto completo de análise de dados explorando tendências de contratação, salários, habilidades e modalidades de trabalho no mercado tech brasileiro.

---

## 🎯 Objetivo do Projeto

Este projeto realiza uma **análise exploratória de dados (EDA)** sobre o mercado de trabalho em tecnologia no Brasil, cobrindo o período de 2024 a 2026. A proposta é responder perguntas-chave que recrutadores, profissionais e candidatos fazem diariamente:

- Quais cargos estão mais em demanda?
- Qual a faixa salarial por cargo e senioridade?
- Quais habilidades técnicas são mais requisitadas?
- Como evoluíram as contratações ao longo do tempo?
- Qual a predominância do trabalho remoto vs presencial?

---

## 📁 Estrutura do Projeto

```
projeto-analise-mercado-tech/
│
├── README.md                          ← Este arquivo
├── data/
│   └── vagas_tech_brasil_2024_2026.csv  ← Dataset com 2.000 vagas
│
├── scripts/
│   ├── 01_gerar_dados.py              ← Geração do dataset sintético
│   ├── 02_analise_exploratoria.py     ← Análise + visualizações
│   └── 03_gerar_excel.py             ← Dashboard Excel formatado
│
├── visualizations/
│   ├── 01_vagas_por_cargo.png
│   ├── 02_salario_cargo_senioridade.png
│   ├── 03_evolucao_trimestral.png
│   ├── 04_modalidade_trabalho.png
│   ├── 05_habilidades_demandadas.png
│   ├── 06_distribuicao_salarial.png
│   ├── 07_heatmap_estado_cargo.png
│   ├── 08_competicao_por_vaga.png
│   ├── 09_ingles_por_senioridade.png
│   └── 10_salario_por_setor.png
│
└── output/
    └── analise_mercado_tech_2024_2026.xlsx  ← Dashboard Excel completo
```

---

## 🔍 Metodologia

### 1. Geração do Dataset (`01_gerar_dados.py`)

O dataset simula **2.000 vagas de emprego** em tecnologia coletadas de plataformas de recrutamento (LinkedIn, Glassdoor, Indeed). As distribuições são baseadas em dados reais do mercado brasileiro:

- **10 cargos** diferentes (Analista de Dados, Cientista de Dados, Engenheiro de Dados, Desenvolvedor Backend/Frontend/Full Stack, Eng. ML, DevOps, PM, UX Designer)
- **4 níveis de senioridade** (Júnior, Pleno, Sênior, Especialista/Lead)
- **3 modalidades** de trabalho (Remoto, Híbrido, Presencial)
- **11 estados** brasileiros com distribuição proporcional ao mercado real
- **12 setores** da economia (Fintech, SaaS, E-commerce, etc.)
- **8 trimestres** (Q1/2024 a Q4/2025)

O cálculo salarial considera multiplicadores realistas por senioridade (0.65x–1.85x), porte da empresa (0.90x–1.25x) e estado (0.85x–1.15x), com variação aleatória de ±12%.

### 2. Análise Exploratória (`02_analise_exploratoria.py`)

Foram geradas **10 visualizações** com matplotlib, seguindo uma paleta de cores validada para acessibilidade (incluindo daltonismo). Cada gráfico responde a uma pergunta específica:

| # | Visualização | Pergunta que Responde |
|---|---|---|
| 01 | Distribuição por Cargo | Quais cargos têm mais vagas abertas? |
| 02 | Salário por Cargo × Senioridade | Quanto ganha cada perfil profissional? |
| 03 | Evolução Trimestral | O mercado está crescendo ou retraindo? |
| 04 | Modalidade de Trabalho | Remoto, híbrido ou presencial domina? |
| 05 | Top 15 Habilidades | Quais skills devo aprender? |
| 06 | Boxplot Salarial | Qual a dispersão salarial por cargo? |
| 07 | Heatmap Estado × Cargo | Onde estão as vagas por região? |
| 08 | Competição por Vaga | Quais cargos têm mais concorrência? |
| 09 | Inglês por Senioridade | Inglês é mais exigido em que nível? |
| 10 | Salário por Setor | Quais setores pagam melhor? |

### 3. Dashboard Excel (`03_gerar_excel.py`)

Workbook profissional com **6 abas**:

| Aba | Conteúdo |
|---|---|
| Resumo Executivo | KPIs principais + insights |
| Dados Brutos | Dataset completo (2.000 linhas) |
| Análise por Cargo | Estatísticas agregadas por cargo |
| Análise por Senioridade | Comparativo entre níveis |
| Habilidades | Ranking das 25 skills mais demandadas |
| Evolução Trimestral | Tendências temporais |

---

## 📈 Principais Descobertas

### Mercado de Trabalho
- **Analista de Dados** é o cargo mais demandado (390 vagas, 19.5% do total)
- O **trabalho remoto** domina com 43.1% das vagas, seguido pelo híbrido (38%)
- Há **tendência de crescimento** nas contratações ao longo dos trimestres

### Salários
- Salário médio geral: **R$ 9.163/mês**
- Salário mediano geral: **R$ 8.500/mês**
- **Gap salarial** Júnior → Sênior: ~129% de aumento
- Engenheiros de Machine Learning têm os maiores salários (mediana acima de R$ 10.000)
- Empresas de grande porte pagam em média **25% a mais** que startups

### Habilidades
- **SQL** é a habilidade #1 (presente em ~48% das vagas)
- **Python** aparece em segundo lugar, essencial para dados e backend
- **Docker** cresce como requisito obrigatório para DevOps e backend
- **54.8%** das vagas exigem inglês

### Competição
- Média de **85 candidatos por vaga**
- Tempo médio para fechar uma posição: ~30 dias

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| **Python 3.x** | Linguagem principal |
| **pandas** | Manipulação e análise de dados |
| **NumPy** | Computação numérica e geração de dados |
| **matplotlib** | Criação de visualizações |
| **seaborn** | Visualizações estatísticas complementares |
| **openpyxl** | Geração do dashboard Excel |

---

## 🚀 Como Executar

```bash
# 1. Clone o repositório
git clone https://github.com/seu-usuario/analise-mercado-tech.git
cd analise-mercado-tech

# 2. Instale as dependências
pip install pandas numpy matplotlib seaborn openpyxl

# 3. Gere o dataset
cd scripts
python 01_gerar_dados.py

# 4. Execute a análise e gere os gráficos
python 02_analise_exploratoria.py

# 5. Gere o dashboard Excel
python 03_gerar_excel.py
```

---

## 💡 Habilidades Demonstradas

Este projeto demonstra domínio em:

- **Coleta e modelagem de dados** — criação de datasets sintéticos com distribuições realistas
- **Limpeza e transformação** — tratamento de dados categóricos, numéricos e textuais
- **Análise exploratória (EDA)** — estatísticas descritivas, correlações, segmentações
- **Visualização de dados** — gráficos profissionais com paleta acessível e tipografia limpa
- **Storytelling com dados** — transformar números em insights acionáveis
- **Automação** — pipeline reprodutível de dados → análise → output
- **Excel avançado** — dashboards formatados profissionalmente com openpyxl

---

## 📝 Licença

Este projeto é de uso livre para fins de estudo e portfólio.

---

*Projeto desenvolvido como portfólio de Data Analytics — Danilo Santos, 2026*
