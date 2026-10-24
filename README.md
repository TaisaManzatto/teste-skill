# 🏭 Análise de Tempo Improdutivo de Máquinas Industriais

Este projeto realiza a análise automatizada de ocorrências e paradas de máquinas em ambiente fabril, identificando as principais causas de indisponibilidade, comparando resultados mensais com metas contratuais e gerando diagnósticos para apoiar planos de ação da manutenção e operação.

O projeto foi construído seguindo as diretrizes e regras analíticas da skill [`analise-tempo`](.agents/skill/analise-tempo/SKILL.md).

---

## 🚀 Tecnologias Utilizadas

O projeto faz uso de ferramentas modernas do ecossistema de análise de dados e inteligência artificial:

- **[Python](https://www.python.org/):** Linguagem principal utilizada para validação, tratamento e cálculos estatísticos.
- **[Pandas](https://pandas.pydata.org/):** Biblioteca para manipulação, agregação tabular, junções de dados mensais e análise de séries temporais.
- **[Matplotlib](https://matplotlib.org/):** Biblioteca para geração de gráficos de alta resolução (Pareto, séries temporais e comparativos de metas).
- **[Git & GitHub](https://github.com/):** Controle de versão e versionamento do histórico de código e relatórios.
- **[Google Antigravity Agentic Framework](https://deepmind.google/):** Estrutura de agentes autônomos com execução baseada em skills padronizadas.

---

## 📊 Estrutura do Projeto

```text
analise-tempo-improdutivo/
├── .agents/
│   └── skill/
│       └── analise-tempo/
│           └── SKILL.md                 # Definição e regras da skill de análise
├── dados/
│   ├── metas_e_horas_planejadas.csv     # Planejamento mensal de horas e metas (%)
│   └── paradas_maquina.csv              # Histórico de ocorrências e durações das paradas
├── resultados/
│   ├── relatorio.md                     # Relatório executivo completo da análise
│   ├── qualidade.md                     # Auditoria de integridade e qualidade das bases
│   ├── pareto_categorias.png            # Gráfico de Pareto por categoria de parada
│   ├── pareto_motivos.png               # Gráfico de Pareto dos top 10 motivos de parada
│   ├── evolucao_temporal.png            # Série histórica mensal de horas paradas
│   ├── comparativo_metas.png            # Desempenho real vs meta (Categorias A, B e C)
│   └── paradas_por_equipamento.png      # Distribuição por máquina (programada vs não programada)
├── .gitignore                           # Exclusão de arquivos temporários e .venv/
├── AGENTS.md                            # Regras de boas práticas e governança do projeto
├── README.md                            # Apresentação do projeto e instruções
└── tempo.py                             # Script de execução da esteira analítica
```

---

## 🔍 Principais Descobertas da Análise

- **Qualidade dos Dados:** 100% íntegra (559 registros de paradas e 44 competências mensais sem nulos, sem duplicatas e sem durações negativas).
- **Volume Total:** 1.098,25 horas de parada frente a 30.429,60 horas planejadas (taxa de indisponibilidade média de **3,61%**).
- **Concentração de Pareto:**
  - A **Categoria A** é a maior geradora de perdas, respondendo por **40,72%** (447,21h) das horas paradas.
  - O motivo individual mais crítico foi **Atividade planejada 01** (112,93h), seguido por **Ocorrência técnica 01** (111,65h).
- **Foco por Equipamento:** O **Equipamento X** concentrou mais da metade de todo o tempo improdutivo da fábrica (**50,84%**).
- **Aderência a Metas:** Apenas a **Categoria A** apresentou desvios frequentes (ultrapassando a meta em **63,6% dos meses** analisados). As Categorias B e C operaram dentro dos limites.

---

## 🛠️ Como Executar o Projeto

1. Clone o repositório:
   ```bash
   git clone https://github.com/TaisaManzatto/teste-skill.git
   cd teste-skill
   ```

2. Crie e ative o ambiente virtual:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

3. Instale as dependências:
   ```bash
   pip install pandas matplotlib
   ```

4. Execute a esteira de análise:
   ```bash
   python tempo.py
   ```

Os relatórios e imagens serão atualizados automaticamente dentro da pasta `resultados/`.

