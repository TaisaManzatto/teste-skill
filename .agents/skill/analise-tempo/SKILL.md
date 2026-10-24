---
name: analise-tempo
description: Analisa bases CSV de horas improdutivas de máquinas industriais, calcula indicadores de indisponibilidade, identifica categorias e motivos de maior impacto, compara períodos e metas e gera gráficos e recomendações baseadas nos dados.
---

# Analisador de Horas Improdutivas de Máquina


---
name: analise-tempo
description: Analisa bases CSV de paradas de máquinas industriais, calcula indicadores de indisponibilidade, identifica categorias e motivos de maior impacto, compara períodos e metas e produz gráficos e recomendações baseadas nos dados.
---

# Machine Downtime Analyzer

## Objetivo
Analisar dados de paradas de máquinas industriais para identificar perdas de produtividade e apoiar decisões de manutenção e produção.

## Fonte de dados
- Procurar arquivos CSV na pasta `dados/`.
- Identificar o arquivo que contém o histórico de paradas.
- Inspecionar as colunas antes de iniciar a análise.
- Identificar o separador, a codificação e o formato das datas.
- Não assumir nomes de colunas sem verificar a estrutura da base.
- Se houver vários arquivos ou dúvidas sobre o significado das colunas, solicitar esclarecimentos.

## Etapas da análise

1. Validar a qualidade dos dados, verificando valores ausentes, duplicidades, datas inválidas e durações inconsistentes.
2. Apresentar um resumo da base: quantidade de registros, período analisado, máquinas e categorias disponíveis.
3. Calcular as horas totais de parada e a participação percentual de cada categoria e motivo.
4. Comparar os resultados entre períodos, quando houver dados suficientes.
5. Comparar os indicadores com as metas, caso estejam disponíveis.
6. Identificar as principais categorias e os motivos com maior impacto nas horas paradas.
7. Gerar gráficos adequados, incluindo evolução temporal e gráfico de Pareto, quando aplicável.
8. Produzir um relatório com resultados, limitações e oportunidades de investigação.

## Regras de análise

- Utilizar Python e Pandas para processamento dos dados.
- Verificar se as durações são numéricas e não negativas.
- Não excluir registros silenciosamente; documentar problemas encontrados.
- Não confundir quantidade de ocorrências com total de horas paradas.
- Calcular percentuais utilizando denominadores claramente definidos.
- Não comparar períodos com bases de cálculo diferentes sem informar a limitação.
- Não inventar metas, causas, valores ou dados ausentes.
- Diferenciar fatos observados, hipóteses e recomendações.
- Não afirmar que uma causa raiz foi identificada apenas com base em correlações.

## Relatório final

Apresentar:
1. Resumo executivo.
2. Qualidade e limitações dos dados.
3. Indicadores calculados e suas fórmulas.
4. Principais categorias e motivos de parada.
5. Gráficos e tendências identificadas.
6. Desvios em relação às metas disponíveis.
7. Perguntas para investigação e recomendações baseadas nas evidências.
8. Salve um resumo em resultados/qualidade.md: problemas encontrados, evidências (números) e tratamentos propostos.

Se não houver dados suficientes para calcular um indicador, explicar o motivo e indicar quais informações são necessárias.
