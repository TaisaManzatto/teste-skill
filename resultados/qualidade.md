# Relatório de Qualidade dos Dados

## 1. Resumo da Verificação de Integridade
A validação de qualidade foi executada de acordo com as diretrizes da skill `analise-tempo`.

- **Total de registros de paradas avaliados:** 559
- **Total de registros de metas/planejamento avaliados:** 44
- **Valores ausentes (nulos) em paradas:** 0
- **Valores ausentes (nulos) em metas:** 0
- **Identificadores (ID_Parada) duplicados:** 0
- **Datas com formato inválido:** 0
- **Durações com valores inconsistentes ou negativos:** 0

## 2. Detalhamento dos Testes Realizados

- Base de paradas: nenhum valor nulo identificado.
- Base de metas: nenhum valor nulo identificado.
- ID_Parada: todos os identificadores sao unicos.
- Nenhuma linha duplicada encontrada em paradas.
- Datas: todos os 559 registros possuem datas validas no formato DD/MM/AAAA.
- Duracoes: nenhuma duracao negativa identificada.
- Horas planejadas: todos os valores sao estritamente positivos.

## 3. Tratamento Proposto e Conclusão
- **Aderência aos dados originais:** Nenhum registro precisou ser descartado ou imputado, pois a base original apresenta integridade completa, sem dados nulos, sem chaves duplicadas e sem durações negativas.
- **Formato temporal:** A coluna `Data` foi convertida com sucesso para o padrão `datetime` utilizando o formato dia/mês/ano (`%d/%m/%Y`) para permitir agregações mensais confiáveis.
- **Classificação:** As categorias e tipos de parada estão padronizados e prontos para agregação.
