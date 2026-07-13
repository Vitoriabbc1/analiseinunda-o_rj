![capa analise](assets/capa.jpg)


## Sobre o Projeto
Este projeto apresenta uma abordagem de inteligência geográfica e análise de dados aplicada à gestão de riscos de desastres hidrológicos no município do Rio de Janeiro. A metodologia consistiu no cruzamento espacial entre a camada shapefile da **Rede Hidrográfica Municipal** e a camada matricial de **Suscetibilidade a Deslizamentos - (Fundação Geo-Rio)** disponibilizada para visualização portal SMAC MAPAS da Prefeitura do Rio de Janeiro.  

O objetivo principal foi quantificar a vulnerabilidade física da infraestrutura de macrodrenagem urbana, categorizando o nível de exposição ao risco (Alta, Média e Baixa Suscetibilidade) para cada tipologia de curso d'água (Rios, Canais, Arroios, Valas e Valões).

*Infraestrutura de Dados Espaciais (IDE)* Devido à ausência de botões de download direto para as bases vetoriais nos portais de origem, foi realizada a extração das URLs dos servidores de mapas oficiais através da análise de requisições de rede. As camadas foram consumidas via conexão nativa WMS/WFS diretamente no ambiente SIG (QGIS), garantindo a integridade e a procedência oficial dos dados consultados.

---

## Tecnologias e Ferramentas Utilizadas
* **QGIS:** Processamento digital de dados vetoriais, operações de interseção espacial e refinamento da base cartográfica.
* **Python (Google Colab):** Tratamento, limpeza de dados textuais estruturados e engenharia de recursos (*feature engineering*) com `Pandas`.
* **Matplotlib & Seaborn:** Geração de gráficos estatísticos avançados e estilização de matrizes de criticidade.

---

## Matriz de Criticidade (Resultados Quantitativos)

A tabela abaixo sintetiza a extensão linear (em quilômetros) e a distribuição percentual de cada tipologia de drenagem frente às classes de suscetibilidade mapeadas[cite: 1, 2]:

| Tipologia do Curso d'Água | Alta Suscetibilidade (km) | Alta (%) | Média Suscetibilidade (km) | Média (%) | Baixa Suscetibilidade (km) | Baixa (%) | Extensão Total (km) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **ARROIO** | 5,43 | 29,74% | 10,10 | 55,31% | 2,73 | 14,95% | **18,26** |
| **CANAL** | 48,85 | 15,51% | 98,06 | 31,13% | 168,09 | 53,36% | **315,00** |
| **RIO** | 139,03 | 15,93% | 272,67 | 31,25% | 460,93 | 52,82% | **872,63** |
| **VALA** | 9,04 | 18,16% | 5,91 | 11,87% | 34,83 | 69,97% | **49,78** |
| **VALÃO** | 0,00 | 0,00% | 0,99 | 6,61% | 13,98 | 93,39% | **14,97** |

---

## Visualização dos Dados

![grafico1](assets/grafico1.png)

---

## Principais Insights Técnicos

* **Pressão Absoluta nos Rios Naturais:** Embora a classe de Alta Suscetibilidade represente cerca de 15,93% da malha dos **Rios**, esse percentual equivale a expressivos **139,03 km** de leitos fluviais correndo sob risco máximo de transbordo urbano, evidenciando o severo adensamento sobre as planícies de inundação naturais (MIRANDA, 2016) 
* **Gargalos de Engenharia nos Canais:** Os **Canais** artificiais somam **48,85 km** em zonas de Alta Suscetibilidade e **98,06 km** em áreas Médias. Praticamente metade (46,64%) de toda a estrutura de engenharia cinza construída para retificação fluviométrica encontra-se em zonas propensas a colapsos micro e macro-hidráulicos.
* **Vulnerabilidade Proporcional dos Arroios:** A tipologia **Arroio** revelou-se a mais sufocada da malha urbana, com **85,05%** de sua extensão total classificada entre Média e Alta Suscetibilidade (55,31% e 29,74%, respectivamente), atuando como os primeiros indicadores de saturação hídrica das bacias.

---

## Diretrizes e Soluções Propostas

Os dados quantitativos robustecem a necessidade de uma transição nos modelos tradicionais de drenagem urbana voltados para a engenharia cinza (canalizações fechadas e concretadas)[cite: 1, 2]. Como direcionamento técnico, propõe-se:
1. Adoção de **Soluções Baseadas na Natureza (SBN)** para recuperação da capacidade de infiltração natural do solo urbano [1](https://www.scielo.br/j/urbe/a/54jTFvySqRCgzkwZ44bJj6M/?format=html&lang=pt)
2. Implantação de bacias de amortecimento de cheias e **Parques Lineares Urbanos** integrados [2](https://repositorio.ufc.br/handle/riufc/59019) 
3. Restauração e fiscalização rígida das **Faixas Marginais de Proteção (FMP)** nos trechos identificados sob Alta Suscetibilidade 

---
### 🏙️ Análise de Vulnerabilidade Local (Top 10 Bairros Críticos)

Ao cruzar a malha hidrográfica fragmentada com as regiões administrativas, o modelo isolou os 10 bairros do município do Rio de Janeiro que concentram a maior extensão linear de drenagem sob **Alta Suscetibilidade** à inundação. 

Essa análise espacial permite o direcionamento assertivo de recursos públicos e priorização de obras de manejo de águas pluviais.

---

## Visualização dos Dados por Bairro

![Top 10 Bairros Críticos](assets/bairros.png)

## Autor
* **Vitória B. B. de Carvalho** - Bióloga e Analista Ambiental 
* [LinkedIn](https://www.linkedin.com/in/vitoria-b-b-de-carvalho/)
* [E-mail](mailto:vibbarcellos@gmail.com)
