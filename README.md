# Planejamento de Cinturão Verde Urbano: Industrial em Aveiro

## 1. Objetivo do Projeto

Identificar áreas críticas para a implementação de barreiras vegetais (Cinturões Verdes) em zonas industriais de Aveiro, quantificando o impacto social através do mapeamento de edifícios residenciais em zonas de influência direta (500 metros).

## 2. Passo a Passo do Desenvolvimento

### Fase 1: Coleta e Tratamento de Dados

- **Identificação Industrial:** Utilização do plugin QuickOSM para extrair polígonos com a chave `landuse=industrial` em Aveiro.
- **Padronização Geométrica:** Conversão do Sistema de Referência de Coordenadas (SRC) para EPSG:3763 (ETRS89 / Portugal TM06), garantindo que os cálculos de distância fossem feitos em metros e não em graus.

### Fase 2: Análise Espacial (Geoprocessamento)

- **Criação do Amortecimento (Buffer):** Geração de uma zona de influência de 500 metros ao redor das áreas industriais.
- **Cálculo de Área:** Utilização da calculadora de campo para determinar a área total do cinturão, resultando em aproximadamente 41,91 $km^2$.
- **Mapeamento de Edifícios:** Download de dados de construção (`building=yes`) via OpenStreetMap para toda a região de estudo.

### Fase 3: Validação e Refinamento

- **Correção de Erros de Banco de Dados:** Solução de conflitos de gravação (erros de SQLite/OGR) através da exportação estruturada em arquivos GeoPackage (`.gpkg`) em diretórios locais definidos.
- **Cruzamento de Dados (Clip/Selection):** Execução de Seleção por Localização para identificar edifícios que interceptam a zona de 500m.

## 3. Análise Final e Resultados

A análise espacial quantitativa revelou dados fundamentais para a tomada de decisão ambiental em Aveiro:

- **Área de Cobertura Proposta:** O cinturão verde abrange uma extensão de 41,91 $km^2$.
- **Impacto Social Quantificado:** Foram identificados exatamente **446 edifícios** (majoritariamente residenciais) localizados dentro da área de influência industrial.
- **Insight Estratégico:** O número de 446 feições representa os pontos de maior vulnerabilidade, onde a arborização urbana deve ser priorizada para mitigar riscos de poluição e melhorar a qualidade de vida da população local.
